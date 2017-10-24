---
title: Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista Microsoft Dynamics 365 for Salesiin."
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
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="4191b-103">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="4191b-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4191b-104">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="4191b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="4191b-105">Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="4191b-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4191b-106">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="4191b-106">Template and task</span></span>

<span data-ttu-id="4191b-107">Seuraavat mallit ja tehtävät, joilla tuotteet synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editionista (Finance and Operations) Microsoft Dynamics 365 for Salesiin (Sales).</span><span class="sxs-lookup"><span data-stu-id="4191b-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="4191b-108">Mallin nimi: tuotteet (Fin and Opsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="4191b-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="4191b-109">Projektin tehtävän nimi: tuotteet</span><span class="sxs-lookup"><span data-stu-id="4191b-109">Name of task in project: Products</span></span>

<span data-ttu-id="4191b-110">Ennen tuotteen synkronointia synkronoitavat tehtävät: ei mitään</span><span class="sxs-lookup"><span data-stu-id="4191b-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="4191b-111">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="4191b-111">Entity set</span></span>

| <span data-ttu-id="4191b-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="4191b-112">**Finance and Operations**</span></span> | <span data-ttu-id="4191b-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="4191b-113">**CDS**</span></span> | <span data-ttu-id="4191b-114">**myynti**</span><span class="sxs-lookup"><span data-stu-id="4191b-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="4191b-115">Myytävät vapautetut tuotteet</span><span class="sxs-lookup"><span data-stu-id="4191b-115">Sellable released products</span></span> | <span data-ttu-id="4191b-116">Tuote</span><span class="sxs-lookup"><span data-stu-id="4191b-116">Product</span></span> | <span data-ttu-id="4191b-117">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="4191b-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4191b-118">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="4191b-118">Entity flow</span></span>

<span data-ttu-id="4191b-119">Tuotteita hallitaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="4191b-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="4191b-120">Finance and Operationsin tietoyksikkö **Myytävät vapautetut tuotteet** vie vain myytävät tuotteet, joten tuotteissa on tietoja, joita tarvitaan myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="4191b-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="4191b-121">Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="4191b-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="4191b-122">**Tuotenumero** toimii avaimena; toisin sanoen tuotevariantit synkronoidaan CDS:ään ja Salesiin siten, kullakin **tuotevariantilla** on oma **tuotetunnus**.</span><span class="sxs-lookup"><span data-stu-id="4191b-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4191b-123">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="4191b-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4191b-124">Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="4191b-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="4191b-125">Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="4191b-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="4191b-126">**On ulkoisesti ylläpidetty = Kyllä**: tuote on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.</span><span class="sxs-lookup"><span data-stu-id="4191b-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="4191b-127">**On ulkoisesti ylläpidetty = Ei**: tuote kirjataan suoraan Salesissa.</span><span class="sxs-lookup"><span data-stu-id="4191b-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="4191b-128">**On ulkoisesti ylläpidetty = tyhjä**: tuote sijaitsee Salesissa ennen ratkaisua prospektista käteiseksi.</span><span class="sxs-lookup"><span data-stu-id="4191b-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="4191b-129">**On ulkoisesti ylläpidetty** -tiedoilla voidaan varmistaa, että vain sellaiset **tarjoukset** ja **myyntitilaukset**, joissa on valittu **Ulkoisesti ylläpidetyt tuotteet**, synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="4191b-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="4191b-130">**Ulkoisesti ylläpidetyt tuotteet** lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan **hinnastoon**.</span><span class="sxs-lookup"><span data-stu-id="4191b-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="4191b-131">Huomaa, että luettelo on järjestetty aakkosjärjestykseen **nimen** mukaan.</span><span class="sxs-lookup"><span data-stu-id="4191b-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="4191b-132">Tuotteen Finance and Operationsin myyntihintaa käytetään **hinnaston** hintana.</span><span class="sxs-lookup"><span data-stu-id="4191b-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="4191b-133">Tämän vuoksi Salesissa on oltava **hinnasto** jokaiselle Finance and Operationsin **tuotteen myyntivaluutalle**.</span><span class="sxs-lookup"><span data-stu-id="4191b-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="4191b-134">Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.</span><span class="sxs-lookup"><span data-stu-id="4191b-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="4191b-135">Tuotteen synkronointi ei onnistu, jos **hinnaston** valuutta ei täsmää.</span><span class="sxs-lookup"><span data-stu-id="4191b-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4191b-136">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="4191b-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="4191b-137">Täytä Finance and Operationsin aiemmin luotujen tuotteiden **Erillisen tuotteen taulu** ennen ensimmäistä synkronointia.</span><span class="sxs-lookup"><span data-stu-id="4191b-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="4191b-138">Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="4191b-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="4191b-139">Etsi **Täytä erillisen tuotteen taulu** Finance and Operationsin hakutoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="4191b-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="4191b-140">Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**.</span><span class="sxs-lookup"><span data-stu-id="4191b-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="4191b-141">Tämä työ on suoritettava vain kerran.</span><span class="sxs-lookup"><span data-stu-id="4191b-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="4191b-142">Varmista, että tarvittava Finance and Operationsin myynnin **mittayksikön** **ValueMap** sijaitsee kohdassa **Lähde -\> CDS-yhdistäminen SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="4191b-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="4191b-143">Päivitä **CDS-organisaation tunnus Organization_OrganizationId** valitsemalla **Lähde -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="4191b-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="4191b-144">Oletusmallin arvo palautetaan oletusarvoon ORG001.</span><span class="sxs-lookup"><span data-stu-id="4191b-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="4191b-145">Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) **ValueMap** kohdassa **CDS -\> Kohde** siten, että se vastaa Salesin **Yksikköryhmiä**.</span><span class="sxs-lookup"><span data-stu-id="4191b-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="4191b-146">Mallin arvo palautetaan oletusarvoon **Oletusyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="4191b-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="4191b-147">Varmista **CDS-keräilyluettelot**-arvon avulla, että kaikkien Finance and Operationsin tuotteiden myynnin mittayksiköt ovat Salesissa.</span><span class="sxs-lookup"><span data-stu-id="4191b-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="4191b-148">Varmista, että Salesissa on **hinnasto** jokaiselle Finance and Operationsin tuotteen myyntivaluutalle.</span><span class="sxs-lookup"><span data-stu-id="4191b-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="4191b-149">Salesissa luotavien tuotteiden tila voi olla **Luonnos** tai **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="4191b-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="4191b-150">Sitä hallitaan valitsemalla Salesissa **Järjestelmäasetukset** **Sales**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="4191b-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="4191b-151">Luonnos-tilassa olevat luodut tuotteet on aktivoitava, ennen kuin ne voidaan lisätä **tarjoukseen** tai **myyntitilaukseen**.</span><span class="sxs-lookup"><span data-stu-id="4191b-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4191b-152">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="4191b-152">Template mapping in data integrator</span></span>

<span data-ttu-id="4191b-153">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="4191b-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![mallin yhdistäminen tietojen integrointiohjelmassa](./media/products-template-mapping-data-integrator-1.png)

![mallin yhdistäminen tuotteita varten tietojen integrointiohjelmassa](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4191b-156">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="4191b-156">Related topics</span></span>

[<span data-ttu-id="4191b-157">Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="4191b-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="4191b-158">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="4191b-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="4191b-159">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="4191b-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="4191b-160">Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="4191b-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="4191b-161">Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="4191b-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


