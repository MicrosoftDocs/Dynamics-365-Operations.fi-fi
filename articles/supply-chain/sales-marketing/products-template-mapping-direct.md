---
title: Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 85ea6d37079c965ac5ddfdc4cdd20f2f3d184e4f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216082"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="d4daf-103">Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="d4daf-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d4daf-104">Tutustu [Common Data Service for Appsin tietojen integrointiin](https://docs.microsoft.com/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="d4daf-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="d4daf-105">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tuotteita synkronoidaan suoraan Dynamics 365 Supply Chain Managementista Dynamics 365 Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="d4daf-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="d4daf-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="d4daf-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="d4daf-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="d4daf-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="d4daf-109">Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="d4daf-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="d4daf-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="d4daf-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d4daf-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="d4daf-111">Templates and tasks</span></span>

<span data-ttu-id="d4daf-112">Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="d4daf-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="d4daf-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="d4daf-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d4daf-114">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan tuotteet Supply Chain Managementista Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="d4daf-115">**Mallin nimi tietojen integroinnissa:** Tuotteet (Supply Chain Managementista Salesiin) – suora</span><span class="sxs-lookup"><span data-stu-id="d4daf-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="d4daf-116">**Tehtävän nimi tietojen integrointiprojektissa:** Tuotteet</span><span class="sxs-lookup"><span data-stu-id="d4daf-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="d4daf-117">Synkronointitehtävät on suoritettava, ennen kuin tuotteen synkronointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="d4daf-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d4daf-118">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="d4daf-118">Entity set</span></span>

| <span data-ttu-id="d4daf-119">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="d4daf-119">Supply Chain Management</span></span>    | <span data-ttu-id="d4daf-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="d4daf-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="d4daf-121">Myytävät vapautetut tuotteet</span><span class="sxs-lookup"><span data-stu-id="d4daf-121">Sellable released products</span></span> | <span data-ttu-id="d4daf-122">Tuotteet</span><span class="sxs-lookup"><span data-stu-id="d4daf-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d4daf-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="d4daf-123">Entity flow</span></span>

<span data-ttu-id="d4daf-124">Tuotteita hallitaan Supply Chain Managementissa ja synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="d4daf-125">**Myytävät vapautetut tuotteet** -tietoyksikkö Supply Chain Managementissa vie vain tuotteet, jotka ovat *myytävissä*.</span><span class="sxs-lookup"><span data-stu-id="d4daf-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="d4daf-126">Myytävissä olevat tuotteet ovat tuotteita, joille on määritetty tiedot myyntitilauksessa käyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="d4daf-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="d4daf-127">Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautettu tuote** -sivun **Vahvista**-toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="d4daf-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="d4daf-128">Tuotenumeroa käytetään avaimena.</span><span class="sxs-lookup"><span data-stu-id="d4daf-128">The product number is used as a key.</span></span> <span data-ttu-id="d4daf-129">Tämän vuoksi jokaisella tuotevariantilla on oltava yksilöivä tuotetunnus, kun tuotevariantit synkronoidaan Salesiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d4daf-130">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="d4daf-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="d4daf-131">Salesissa tuotteisiin on lisätty uusi **On ulkoisesti ylläpidetty** -kenttä ilmaisemaan, että annettua tuotetta ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="d4daf-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="d4daf-132">Arvoksi valitaan oletusarvoisesti **Kyllä** Salesiin tuonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="d4daf-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="d4daf-133">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="d4daf-133">The following values are available:</span></span>

- <span data-ttu-id="d4daf-134">**Kyllä** – Tuote on peräisin Supply Chain Managementista eikä sitä voi muokata Salesissa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="d4daf-135">**Ei** – tuote kirjataan suoraan Salesissa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="d4daf-136">**(Tyhjä)** – tuote sijaitsi Salesissa ennen Prospektista käteiseksi -ratkaisun käyttöönottoa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="d4daf-137">**On ulkoisesti ylläpidetty** -kenttä auttaa varmistamaan, että Supply Chain Managementiin synkronoidaan vain tarjoukset ja myyntitilaukset, joissa on ulkoisesti ylläpidettyjä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="d4daf-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="d4daf-138">Ulkoisesti ylläpidetyt tuotteet lisätään automaattisesti ensimmäiseen samaa valuuttaa käyttävään ja voimassa olevaan hinnastoon.</span><span class="sxs-lookup"><span data-stu-id="d4daf-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="d4daf-139">Hinnastot järjestetään aakkosjärjestykseen nimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4daf-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="d4daf-140">Tuotteen Supply Chain Managementin myyntihintaa käytetään hinnaston hintana.</span><span class="sxs-lookup"><span data-stu-id="d4daf-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="d4daf-141">Tämän vuoksi Salesissa on oltava hinnasto jokaiselle Supply Chain Managementin tuotteen myyntivaluutalle.</span><span class="sxs-lookup"><span data-stu-id="d4daf-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="d4daf-142">Vapautettujen myytävien tuotteiden valuutta on määritetty sen yrityksen tilivaluutaksi, josta tuote viedään.</span><span class="sxs-lookup"><span data-stu-id="d4daf-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="d4daf-143">Tuotteen synkronointi ei onnistu, jos hinnastossa ei ole vastaavaa valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="d4daf-144">Voit määrittää integroinnissa käytettävän hinnaston yhdistämällä pricelevelid.name [oletus hinnasto (nimi)] tietojen integrointiprojektiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="d4daf-145">Syötteen on oltava pienillä kirjaimilla.</span><span class="sxs-lookup"><span data-stu-id="d4daf-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="d4daf-146">Esimerkiksi oletusarvoinen myynnin Vakio-niminen hinnasto voisi olla kohdekenttä: pricelevelid.name [Oletusarvoinen hinnasto (Nimi)] ja karttatyyppi: [ { ”transformType”: ”Default", "defaultValue": "standard} ].</span><span class="sxs-lookup"><span data-stu-id="d4daf-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d4daf-147">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="d4daf-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="d4daf-148">Täytä Supply Chain Managementin aiemmin luotujen tuotteiden erillisen tuotteen taulu ennen ensimmäistä synkronointia.</span><span class="sxs-lookup"><span data-stu-id="d4daf-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="d4daf-149">Aiemmin luotuja tuotteita ei synkronoida, ennen kuin tämä työ on valmis.</span><span class="sxs-lookup"><span data-stu-id="d4daf-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="d4daf-150">Etsi **Täytä erillisen tuotteen taulu** Supply Chain Managementin hakutoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="d4daf-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="d4daf-151">Suorita työ valitsemalla **Täytä erillisen tuotteen taulu**.</span><span class="sxs-lookup"><span data-stu-id="d4daf-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="d4daf-152">Tämän työn voi suorittaa vain kerran.</span><span class="sxs-lookup"><span data-stu-id="d4daf-152">This job must be run only one time.</span></span>

- <span data-ttu-id="d4daf-153">Varmista, että Supply Chain Managementin ja Salesin välillä on myynnin mittayksikön arvokartta **SalesUnitSymbol**- ja **DefaultUnit (Name)**-kohteen väliselle yhdistämismääritykselle.</span><span class="sxs-lookup"><span data-stu-id="d4daf-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="d4daf-154">Päivitä **yksikköryhmän** (**defaultuomscheduleid.name**) arvomääritys siten, että se vastaa Salesin **yksikköryhmiä**.</span><span class="sxs-lookup"><span data-stu-id="d4daf-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="d4daf-155">Oletusmallin arvo on **Oletusyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="d4daf-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="d4daf-156">Varmista, että kaikkien Supply Chain Managementin tuotteiden myynnin mittayksiköt ovat Salesissa.</span><span class="sxs-lookup"><span data-stu-id="d4daf-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="d4daf-157">Varmista, että Salesissa on hinnasto jokaiselle Supply Chain Managementin tuotteen myyntivaluutalle.</span><span class="sxs-lookup"><span data-stu-id="d4daf-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="d4daf-158">Kun tuotteet luodaan Salesissa, niiden tila on **Luonnos** tai **Aktiivinen**.</span><span class="sxs-lookup"><span data-stu-id="d4daf-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="d4daf-159">Toimintaa ohjataan Salesissa kohdassa **Asetukset** > **Hallinto** > **Järjestelmäasetukset** > **Sales**.</span><span class="sxs-lookup"><span data-stu-id="d4daf-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="d4daf-160">Tuotteet, joiden tila on **Luonnos** luomisen jälkeen, on aktivoitava ennen tarjouksiin tai myyntitilauksiin lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="d4daf-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d4daf-161">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="d4daf-161">Template mapping in Data integration</span></span>

<span data-ttu-id="d4daf-162">Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="d4daf-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="d4daf-163">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="d4daf-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="d4daf-165">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="d4daf-165">Related topics</span></span>

[<span data-ttu-id="d4daf-166">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="d4daf-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="d4daf-167">Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="d4daf-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="d4daf-168">Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="d4daf-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="d4daf-169">Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä</span><span class="sxs-lookup"><span data-stu-id="d4daf-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="d4daf-170">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin</span><span class="sxs-lookup"><span data-stu-id="d4daf-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



