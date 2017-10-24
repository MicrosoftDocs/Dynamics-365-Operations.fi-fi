---
title: Sales-tilien synkronointi Finance and Operationsin asiakkaille
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin tilit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="4cd1f-103">Sales-tilien synkronointi Finance and Operationsin asiakkaille</span><span class="sxs-lookup"><span data-stu-id="4cd1f-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4cd1f-104">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="4cd1f-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin tilit (Sales) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="4cd1f-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4cd1f-106">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="4cd1f-106">Template and task</span></span>

<span data-ttu-id="4cd1f-107">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan tilit Salesista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="4cd1f-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="4cd1f-108">**Mallin nimi:** tilit (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="4cd1f-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="4cd1f-109">**Projektin tehtävän nimi:** tilit – tili – asiakkaat</span><span class="sxs-lookup"><span data-stu-id="4cd1f-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="4cd1f-110">Ennen tilin tarvittavat tehtävät synkronoidaan / asiakkaan synkronoida: ei mitään</span><span class="sxs-lookup"><span data-stu-id="4cd1f-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="4cd1f-111">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="4cd1f-111">Entity set</span></span>

| <span data-ttu-id="4cd1f-112">Myynti</span><span class="sxs-lookup"><span data-stu-id="4cd1f-112">Sales</span></span>    | <span data-ttu-id="4cd1f-113">CDS</span><span class="sxs-lookup"><span data-stu-id="4cd1f-113">CDS</span></span>     | <span data-ttu-id="4cd1f-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4cd1f-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="4cd1f-115">Tilit</span><span class="sxs-lookup"><span data-stu-id="4cd1f-115">Accounts</span></span> | <span data-ttu-id="4cd1f-116">Tili</span><span class="sxs-lookup"><span data-stu-id="4cd1f-116">Account</span></span> | <span data-ttu-id="4cd1f-117">Asiakkaat</span><span class="sxs-lookup"><span data-stu-id="4cd1f-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="4cd1f-118">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="4cd1f-118">Entity flow</span></span>

<span data-ttu-id="4cd1f-119">Summia hallitaan Salesissa ja synkronoidaan Finance and Operationsiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="4cd1f-120">Näiden asiakkaiden **On ulkoisesti ylläpidetty** -ominaisuuden arvoksi on määritetty **Kyllä**, jotta Salesista peräisin olevia asiakkaita voidaan jäljittää.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="4cd1f-121">Näitä tietoja käytetään suodattamaan Salesiin synkronoitavat laskut laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4cd1f-122">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="4cd1f-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4cd1f-123">**Tilinumero**-kenttä on käytettävissä **Tili**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="4cd1f-124">Se on nyt luontainen ja yksilöllinen integrointia tukeva avain.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="4cd1f-125">Asiakkuudenhallinta- eli CRM-ratkaisun luonnollinen avain -ominaisuudella voi olla vaikutusta asiakkaisiin, jotka käyttävät jo **Tilinumero**-kenttää mutta eivät yksilöllisiä tilikohtaisia **Tilinumero**-arvoja.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="4cd1f-126">Integrointiratkaisu ei tue tätä tapausta tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="4cd1f-127">Jos **Tilinumero**-arvoa ei ole vielä luotu, kun uusi tili luodaan, se luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="4cd1f-128">Arvossa on ensimmäisenä **ACC**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="4cd1f-129">Esimerkki: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="4cd1f-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="4cd1f-130">Kun Salesin integrointiratkaisua käytetään, päivityskomentosarja määrittää aiemmin Salesissa luotujen tilien **Tilinumero**-kentän.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="4cd1f-131">Jos **Tilinumero**-arvoja ei ole, käytetään edellä kuvattua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4cd1f-132">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="4cd1f-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="4cd1f-133">**CustomerGroupId**-yhdistämismääritys **CDS &gt; Kohde** on päivitettävä Finance and Operationsin kelvolliseksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-134">Voit määrittää oletusarvon. Vaihtoehtoisesti voit määrittää arvon arvomäärityksellä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="4cd1f-135">Oletusmallin arvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-135">The default template value is **10**.</span></span>
- <span data-ttu-id="4cd1f-136">**Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-137">Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="4cd1f-138">Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="4cd1f-139">Mallin **AddressCountryRegionISOCode** oletusarvo on **USA**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="4cd1f-140">Mallin **DeliveryAddressCountryRegionISOCode** oletusarvo on **USA**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="4cd1f-141">Kun seuraavat yhdistämismääritykset lisätään kohdasta **CDS &gt; Kohde**, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-142">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="4cd1f-143">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-144">Oletustoimipaikka voidaan ottaa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="4cd1f-145">Mallin **SiteId** oletusarvo on **1**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="4cd1f-146">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-147">Oletusvarasto voidaan ottaa Finance and Operationsissa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-148">Mallin **WarehouseId** oletusarvo on **13**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="4cd1f-149">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="4cd1f-150">Oletusarvoisesti käytetään asiakkaan tilausotsikon kieltä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="4cd1f-151">Mallin **LanguageId** oletusarvo on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="4cd1f-152">Päivitä CDS-organisaation tunnus (**Organization_OrganizationId**) **Lähde &gt; CDS** -yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="4cd1f-153">Oletusmallin arvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4cd1f-154">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="4cd1f-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="4cd1f-155">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="4cd1f-156">Näiden kenttien yhdistämistä varten on määritettävä arvomääritys.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="4cd1f-157">Arvomääritykset koskevat niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="4cd1f-158">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="4cd1f-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/accounts-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tilejä varten tietojen integrointiohjelmassa](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4cd1f-161">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="4cd1f-161">Related topics</span></span>

[<span data-ttu-id="4cd1f-162">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="4cd1f-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="4cd1f-163">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="4cd1f-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="4cd1f-164">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="4cd1f-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="4cd1f-165">Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="4cd1f-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="4cd1f-166">Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="4cd1f-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




