---
title: Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Salesiin.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: feb9fbc066162e2caa9fc5dbaeec2c063ae23060
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "348247"
---
# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="99868-103">Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="99868-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="99868-104">Tutustu [Common Data Service for Appsin tietojen integrointiin](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="99868-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="99868-105">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Salesiin.</span><span class="sxs-lookup"><span data-stu-id="99868-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="99868-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="99868-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="99868-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="99868-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="99868-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="99868-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="99868-109">Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="99868-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="99868-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="99868-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="99868-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="99868-111">Templates and tasks</span></span>

<span data-ttu-id="99868-112">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="99868-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="99868-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="99868-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="99868-114">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan tuotteet Finance and Operationsista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="99868-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="99868-115">**Mallin nimi tietojen integroinnissa:** Tuotteet (Fin and Opsista Salesiin) – suora</span><span class="sxs-lookup"><span data-stu-id="99868-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="99868-116">**Tehtävän nimi tietojen integrointiprojektissa:** Tuotteet</span><span class="sxs-lookup"><span data-stu-id="99868-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="99868-117">Synkronointitehtävät on suoritettava, ennen kuin tuotteen synkronointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="99868-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="99868-118">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="99868-118">Entity set</span></span>

| <span data-ttu-id="99868-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="99868-119">Finance and Operations</span></span>     | <span data-ttu-id="99868-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="99868-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="99868-121">Myytävät vapautetut tuotteet</span><span class="sxs-lookup"><span data-stu-id="99868-121">Sellable released products</span></span> | <span data-ttu-id="99868-122">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="99868-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="99868-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="99868-123">Entity flow</span></span>

<span data-ttu-id="99868-124">Tuotteita hallitaan Finance and Operationsissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="99868-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="99868-125">**Myytävät vapautetut tuotteet** -tietoyksikkö Finance and Operationsissa vie vain tuotteet, jotka ovat *myytävissä*.</span><span class="sxs-lookup"><span data-stu-id="99868-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="99868-126">Myytävissä olevat tuotteet ovat tuotteita, joille on määritetty tiedot myyntitilauksessa käyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="99868-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="99868-127">Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="99868-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="99868-128">Tuotenumeroa käytetään avaimena.</span><span class="sxs-lookup"><span data-stu-id="99868-128">The product number is used as a key.</span></span> <span data-ttu-id="99868-129">Tämän vuoksi jokaisella tuotevariantilla on oltava yksilöivä tuotetunnus, kun tuotevariantit synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="99868-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="99868-130">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="99868-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="99868-131">Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="99868-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="99868-132">Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="99868-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="99868-133">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="99868-133">The following values are available:</span></span>

- <span data-ttu-id="99868-134">**Kyllä** – tuote on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.</span><span class="sxs-lookup"><span data-stu-id="99868-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="99868-135">**Ei** – tuote kirjataan suoraan Salesissa.</span><span class="sxs-lookup"><span data-stu-id="99868-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="99868-136">**(Tyhjä)** – tuote sijaitsi Salesissa ennen Prospektista käteiseksi -ratkaisun käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="99868-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="99868-137">**On ulkoisesti ylläpidetty** -kentän avulla voidaan varmistaa, että vain sellaiset tarjoukset ja myyntitilaukset, joissa on ulkoisesti ylläpidettyjä tuotteita, synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="99868-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="99868-138">Ulkoisesti ylläpidetyt tuotteet lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan hinnastoon.</span><span class="sxs-lookup"><span data-stu-id="99868-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="99868-139">Hinnastot järjestetään aakkosjärjestykseen nimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="99868-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="99868-140">Tuotteen Finance and Operationsin myyntihintaa käytetään hinnaston hintana.</span><span class="sxs-lookup"><span data-stu-id="99868-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="99868-141">Tämän vuoksi Salesissa on oltava hinnasto jokaiselle Finance and Operationsin tuotteen myyntivaluutalle.</span><span class="sxs-lookup"><span data-stu-id="99868-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="99868-142">Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.</span><span class="sxs-lookup"><span data-stu-id="99868-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="99868-143">Tuotteen synkronointi ei onnistu, jos hinnastossa ei ole vastaavaa valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="99868-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="99868-144">Voit määrittää integroinnissa käytettävän hinnaston yhdistämällä pricelevelid.name [oletus hinnasto (nimi)] tietojen integrointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="99868-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="99868-145">Syötteen on oltava pienillä kirjaimilla.</span><span class="sxs-lookup"><span data-stu-id="99868-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="99868-146">Esimerkiksi oletusarvoinen myynnin Vakio-niminen hinnasto voisi olla kohdekenttä: pricelevelid.name [Oletusarvoinen hinnasto (Nimi)] ja karttatyyppi: [ { ”transformType”: ”Default", "defaultValue": "standard} ].</span><span class="sxs-lookup"><span data-stu-id="99868-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="99868-147">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="99868-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="99868-148">Täytä Finance and Operationsin aiemmin luotujen tuotteiden erillisen tuotteen taulu ennen ensimmäistä synkronointia.</span><span class="sxs-lookup"><span data-stu-id="99868-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="99868-149">Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="99868-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="99868-150">Etsi **Täytä erillisen tuotteen taulu** Finance and Operationsin hakutoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="99868-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="99868-151">Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**.</span><span class="sxs-lookup"><span data-stu-id="99868-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="99868-152">Tämän työn voi suorittaa vain kerran.</span><span class="sxs-lookup"><span data-stu-id="99868-152">This job must be run only one time.</span></span>

- <span data-ttu-id="99868-153">Varmista, että Finance and Operationsin ja Salesin välillä on myynnin mittayksikön arvokartta **SalesUnitSymbol**- ja **DefaultUnit (Name)**-kohteen väliselle yhdistämismääritykselle.</span><span class="sxs-lookup"><span data-stu-id="99868-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="99868-154">Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) arvomääritys siten, että se vastaa Salesin **yksikköryhmiä**.</span><span class="sxs-lookup"><span data-stu-id="99868-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="99868-155">Oletusmallin arvo on **Oletusyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="99868-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="99868-156">Varmista, että kaikkien Finance and Operationsin tuotteiden myynnin mittayksiköt ovat Salesissa.</span><span class="sxs-lookup"><span data-stu-id="99868-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="99868-157">Varmista, että Salesissa on hinnasto jokaiselle Finance and Operationsin tuotteen myyntivaluutalle.</span><span class="sxs-lookup"><span data-stu-id="99868-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="99868-158">Kun tuotteet luodaan Salesissa, niiden tila on **Luonnos** tai **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="99868-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="99868-159">Toimintaa ohjataan Salesissa kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales**.</span><span class="sxs-lookup"><span data-stu-id="99868-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="99868-160">Tuotteet, joiden tila on **Luonnos** luomisen jälkeen, on aktivoitava ennen tarjouksiin tai myyntitilauksiin lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="99868-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="99868-161">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="99868-161">Template mapping in Data integration</span></span>

<span data-ttu-id="99868-162">Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="99868-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="99868-163">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="99868-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="99868-165">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="99868-165">Related topics</span></span>

[<span data-ttu-id="99868-166">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="99868-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="99868-167">Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="99868-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="99868-168">Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="99868-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="99868-169">Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="99868-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="99868-170">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="99868-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



