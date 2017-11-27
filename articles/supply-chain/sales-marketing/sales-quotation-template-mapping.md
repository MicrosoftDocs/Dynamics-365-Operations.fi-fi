---
title: Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
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
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="70602-103">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="70602-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="70602-104">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="70602-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="70602-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin (Sales) myyntitarjousten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="70602-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="70602-106">Malli ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="70602-106">Template and tasks</span></span>

<span data-ttu-id="70602-107">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntitarjousten otsikot ja rivit Salesista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="70602-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="70602-108">**Mallin nimi:** Myyntitarjoukset (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="70602-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="70602-109">**Projektin tehtävien nimet:**</span><span class="sxs-lookup"><span data-stu-id="70602-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="70602-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="70602-110">QuoteHeader</span></span>
    - <span data-ttu-id="70602-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="70602-111">QuoteLine</span></span>

<span data-ttu-id="70602-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="70602-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="70602-113">Tuotteet (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="70602-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="70602-114">Tilit (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="70602-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="70602-115">Yhteyshenkilöstä asiakkaisiin (Salesista Fin and Opsiin) (jos käytössä)</span><span class="sxs-lookup"><span data-stu-id="70602-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="70602-116">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="70602-116">Entity set</span></span>

| <span data-ttu-id="70602-117">Myynti</span><span class="sxs-lookup"><span data-stu-id="70602-117">Sales</span></span>        | <span data-ttu-id="70602-118">CDS</span><span class="sxs-lookup"><span data-stu-id="70602-118">CDS</span></span>           | <span data-ttu-id="70602-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70602-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="70602-120">Tarjoukset</span><span class="sxs-lookup"><span data-stu-id="70602-120">Quotes</span></span>       | <span data-ttu-id="70602-121">Tarjous</span><span class="sxs-lookup"><span data-stu-id="70602-121">Quotation</span></span>     | <span data-ttu-id="70602-122">Myyntitarjouksen otsikot</span><span class="sxs-lookup"><span data-stu-id="70602-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="70602-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="70602-123">QuoteDetails</span></span> | <span data-ttu-id="70602-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="70602-124">QuotationLine</span></span> | <span data-ttu-id="70602-125">CDS-myyntitarjousrivit</span><span class="sxs-lookup"><span data-stu-id="70602-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="70602-126">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="70602-126">Entity flow</span></span>

<span data-ttu-id="70602-127">Myyntitarjoukset luodaan Salesissa ja synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="70602-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="70602-128">Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="70602-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="70602-129">Kaikkia myyntitarjousrivien tuotteita ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="70602-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="70602-130">Myyntitarjous on aktiivinen tai aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="70602-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="70602-131">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="70602-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="70602-132">**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty tarjousyksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="70602-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="70602-133">Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="70602-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="70602-134">Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.</span><span class="sxs-lookup"><span data-stu-id="70602-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="70602-135">Kaikki tarjouksen tuotteet ja rivit päivitetään tarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="70602-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="70602-136">Nämä tiedot sijaitsevat tarjousriviyksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="70602-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="70602-137">**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="70602-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="70602-138">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="70602-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="70602-139">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä hallitaan Finance and Operationsissa, jossa niitä myös käsitellään.</span><span class="sxs-lookup"><span data-stu-id="70602-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="70602-140">Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="70602-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="70602-141">**Myyntitarjouksen otsikon vain luku -kentät:** Alennusprosentti, Alennus, Rahdin summa</span><span class="sxs-lookup"><span data-stu-id="70602-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="70602-142">**Myyntitarjousrivien vain luku -kentät:** Vero</span><span class="sxs-lookup"><span data-stu-id="70602-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="70602-143">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="70602-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="70602-144">Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntitilausten synkronointia:</span><span class="sxs-lookup"><span data-stu-id="70602-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="70602-145">Asetukset Salesissa</span><span class="sxs-lookup"><span data-stu-id="70602-145">Setup in Sales</span></span>

- <span data-ttu-id="70602-146">Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että **Alennuksen laskutapa** -kentässä on valittu **Yksikköä kohden**.</span><span class="sxs-lookup"><span data-stu-id="70602-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="70602-147">Tällä asetuksella voidaan varmistaa, että Salesin rivinimikkeen alennus vastaa Finance and Operationsin asetusta.</span><span class="sxs-lookup"><span data-stu-id="70602-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="70602-148">Muussa tapauksessa alennus ei ole oikein Finance and Operationsissa, koska Finance and Operations lukee alennuksen yksikkökohtaisena alennuksena, vaikka se oli rivikohtainen alennus Salesissa.</span><span class="sxs-lookup"><span data-stu-id="70602-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="70602-149">Asetukset Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="70602-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="70602-150">Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="70602-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="70602-151">Valitse **Numerojärjestys**-välilehdessä myyntitarjousten numerojärjestys ja valitse sitten **Näytä tiedot**.</span><span class="sxs-lookup"><span data-stu-id="70602-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="70602-152">Valitse sitten **Yleinen asetus** -kohdassa **Manuaalinen**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="70602-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="70602-153">Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="70602-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="70602-154">Valitse sitten **Lähetykset**-välilehden **Toimituspäivän tarkistus** -kentässä **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="70602-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="70602-155">Tämä asetuksen ansiosta synkronointi ei aiheuta myyntitarjousten epäonnistumista.</span><span class="sxs-lookup"><span data-stu-id="70602-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="70602-156">Asetukset tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="70602-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="70602-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="70602-157">QuoteHeader</span></span>

- <span data-ttu-id="70602-158">**Pyydetty toimituspäivämäärä** -kenttä on pakollinen Finance and Operationsissa, ja synkronointi epäonnistuu, jos kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="70602-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="70602-159">Voit estää tämän ongelman, kun kentän ollessa tyhjä oletuspäivämäärä otetaan kohdasta **Lähde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="70602-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="70602-160">Päivämäärä on päivitettävä halutuksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="70602-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="70602-161">Tällä hetkellä kuluvaa päivää ei voi ilmaista arvolla, kuten **Tänään**.</span><span class="sxs-lookup"><span data-stu-id="70602-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="70602-162">Anna tietty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="70602-162">You must enter a specific date.</span></span> <span data-ttu-id="70602-163">Mallin **Pyydetty toimituspäivämäärä** oletusarvo on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="70602-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="70602-164">**Osoitteen maa- tai aluekoodi** -kenttä on pakollinen Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="70602-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="70602-165">Voit estää synkronointivirheet määrittämällä oletusarvon, jota käytetään, jos kenttä on jätetty tyhjäksi Salesissa.</span><span class="sxs-lookup"><span data-stu-id="70602-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="70602-166">Oletusarvo on hyödyllinen myös siksi, ettei paikallisten osoitteiden arvoa tarvitse antaa manuaalisesti **Maa tai alue** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="70602-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="70602-167">Oletusmallin **DeliveryAddressCountryRegionISOCode** -arvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="70602-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="70602-168">Päivitä **CDS-organisaation tunnus** -määritys kohdassa **Lähde &gt; CDS** siten, että se vastaa organisaatioyksikön **CDS-organisaatio**-arvoa:</span><span class="sxs-lookup"><span data-stu-id="70602-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="70602-169">**Organization_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="70602-170">**Account_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="70602-171">**InvoiceAccount_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="70602-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="70602-172">QuoteLine</span></span>

- <span data-ttu-id="70602-173">Päivitä **CDS-organisaation tunnus** -määritys kohdassa **Lähde &gt; CDS** siten, että se vastaa organisaatioyksikön **CDS-organisaatio**-arvoa:</span><span class="sxs-lookup"><span data-stu-id="70602-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="70602-174">**Organization_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="70602-175">**Product_Organization_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="70602-176">**Quotation_Organization_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="70602-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="70602-177">**Pyydetty toimituspäivämäärä** -kenttä on pakollinen Finance and Operationsissa, ja synkronointi epäonnistuu, jos kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="70602-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="70602-178">Voit estää tämän ongelman, kun kentän ollessa tyhjä oletuspäivämäärä otetaan kohdasta **Lähde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="70602-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="70602-179">Päivämäärä on päivitettävä halutuksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="70602-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="70602-180">Tällä hetkellä kuluvaa päivää ei voi ilmaista arvolla, kuten **Tänään**.</span><span class="sxs-lookup"><span data-stu-id="70602-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="70602-181">Anna tietty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="70602-181">You must enter a specific date.</span></span> <span data-ttu-id="70602-182">Mallin **Pyydetty toimituspäivämäärä** oletusarvo on **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="70602-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="70602-183">Voit lisätä seuraavat yhdistämismääritykset kohdasta **CDS &gt; Kohde** ja varmistaa näin, että tarjousrivit tuodaan Finance and Operationsiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:</span><span class="sxs-lookup"><span data-stu-id="70602-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="70602-184">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="70602-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="70602-185">**SiteId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="70602-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="70602-186">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="70602-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="70602-187">**WarehouseId**-oletusmalliarvoa ei ole.</span><span class="sxs-lookup"><span data-stu-id="70602-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="70602-188">Varmista, että Finance and Operationsin myynnin mittayksikön arvokartta on olemassa **CDS &gt; Kohde** -määritykselle, jota käytetään määritettäessä **Quantity_UOM** kohteeseen **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="70602-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="70602-189">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="70602-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="70602-190">**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin.</span><span class="sxs-lookup"><span data-stu-id="70602-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="70602-191">Tämä määritys ei tue tällä hetkellä integrointimääritystä.</span><span class="sxs-lookup"><span data-stu-id="70602-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="70602-192">Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="70602-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="70602-193">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="70602-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="70602-194">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="70602-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="70602-195">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="70602-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="70602-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="70602-196">QuoteHeader</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="70602-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="70602-199">QuoteLine</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="70602-202">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="70602-202">Related topics</span></span>

[<span data-ttu-id="70602-203">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="70602-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="70602-204">Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="70602-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="70602-205">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="70602-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



