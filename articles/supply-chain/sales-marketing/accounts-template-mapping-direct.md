---
title: Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tilejä synkronoidaan suoraan Dynamics 365 Salesista Supply Chain Managementiin.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529207"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="800fa-103">Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="800fa-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="800fa-104">Tutustu [Common Data Service for Appsin tietojen integrointiin](https://docs.microsoft.com/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="800fa-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="800fa-105">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla tilejä synkronoidaan suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="800fa-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="800fa-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="800fa-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="800fa-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="800fa-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="800fa-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="800fa-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="800fa-109">Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="800fa-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="800fa-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="800fa-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="800fa-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="800fa-111">Templates and tasks</span></span>

<span data-ttu-id="800fa-112">Näet käytettävissä olevat mallit avaamalla [Power Apps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="800fa-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="800fa-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="800fa-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="800fa-114">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan tilit Salesista Supply Chain Managementiin:</span><span class="sxs-lookup"><span data-stu-id="800fa-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="800fa-115">**Mallin nimi tietojen integroinnissa:** tilit (Salesista Fin and Opsiin) – suora</span><span class="sxs-lookup"><span data-stu-id="800fa-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="800fa-116">**Projektin tehtävän nimi:** tilit – asiakkaat</span><span class="sxs-lookup"><span data-stu-id="800fa-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="800fa-117">Synkronointitehtävät on suoritettava, ennen kuin tilin ja asiakkaan synkronointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="800fa-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="800fa-118">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="800fa-118">Entity set</span></span>

| <span data-ttu-id="800fa-119">Myynti</span><span class="sxs-lookup"><span data-stu-id="800fa-119">Sales</span></span>    | <span data-ttu-id="800fa-120">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="800fa-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="800fa-121">Tilit</span><span class="sxs-lookup"><span data-stu-id="800fa-121">Accounts</span></span> | <span data-ttu-id="800fa-122">Asiakkaat V2</span><span class="sxs-lookup"><span data-stu-id="800fa-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="800fa-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="800fa-123">Entity flow</span></span>

<span data-ttu-id="800fa-124">Tilejä hallitaan Salesista ja synkronoidaan Supply Chain Managementiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="800fa-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="800fa-125">Näiden asiakkaiden **On ulkoisesti ylläpidetty** -ominaisuuden arvoksi on määritetty **Kyllä**, jotta Salesista peräisin olevia asiakkaita voidaan jäljittää.</span><span class="sxs-lookup"><span data-stu-id="800fa-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="800fa-126">Näitä tietoja käytetään suodattamaan Salesiin synkronoitavat laskut laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="800fa-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="800fa-127">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="800fa-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="800fa-128">**Tilinumero**-kenttä on käytettävissä **Tili**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="800fa-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="800fa-129">Se on nyt luontainen ja yksilöllinen avain, joka tukee integrointia.</span><span class="sxs-lookup"><span data-stu-id="800fa-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="800fa-130">Asiakkuudenhallinta- eli CRM-ratkaisun luonnollinen avain -ominaisuudella voi olla vaikutusta asiakkaisiin, jotka käyttävät jo **Tilinumero**-kenttää mutta eivät yksilöllisiä tilikohtaisia **Tilinumero**-arvoja.</span><span class="sxs-lookup"><span data-stu-id="800fa-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="800fa-131">Integrointiratkaisu ei tue tätä tapausta tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="800fa-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="800fa-132">Jos **Tilinumero**-arvoa ei ole vielä luotu, kun uusi tili luodaan, se luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="800fa-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="800fa-133">Arvossa on ensimmäisenä **ACC**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="800fa-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="800fa-134">Esimerkki: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="800fa-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="800fa-135">Kun Salesin integrointiratkaisua käytetään, päivityskomentosarja määrittää aiemmin Salesissa luotujen tilien **Tilinumero**-kentän.</span><span class="sxs-lookup"><span data-stu-id="800fa-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="800fa-136">Jos **Tilinumero**-arvoja ei ole, käytetään edellä mainittua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="800fa-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="800fa-137">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="800fa-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="800fa-138">**CustomerGroupId**-yhdistämismääritys on päivitettävä Supply Chain Managementin kelvolliseksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="800fa-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="800fa-139">Voit määrittää oletusarvon. Vaihtoehtoisesti voit määrittää arvon arvomäärityksellä.</span><span class="sxs-lookup"><span data-stu-id="800fa-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="800fa-140">Oletusmallin arvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="800fa-140">The default template value is **10**.</span></span>

- <span data-ttu-id="800fa-141">Kun seuraavat yhdistämismääritykset lisätään, Supply Chain Managementissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="800fa-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="800fa-142">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="800fa-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="800fa-143">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="800fa-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="800fa-144">Oletustoimipaikka voidaan ottaa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="800fa-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="800fa-145">Oletusmallin arvo on **1**.</span><span class="sxs-lookup"><span data-stu-id="800fa-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="800fa-146">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="800fa-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="800fa-147">Oletusvarasto voidaan ottaa Supply Chain Managementissa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="800fa-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="800fa-148">Oletusmallin arvo on **13**.</span><span class="sxs-lookup"><span data-stu-id="800fa-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="800fa-149">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="800fa-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="800fa-150">Oletusarvoisesti käytetään asiakkaan tilausotsikon kieltä.</span><span class="sxs-lookup"><span data-stu-id="800fa-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="800fa-151">Oletusmallin arvo on **fi-fi**.</span><span class="sxs-lookup"><span data-stu-id="800fa-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="800fa-152">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="800fa-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="800fa-153">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="800fa-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="800fa-154">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="800fa-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="800fa-155">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="800fa-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="800fa-156">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="800fa-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="800fa-158">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="800fa-158">Related topics</span></span>


[<span data-ttu-id="800fa-159">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="800fa-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="800fa-160">Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="800fa-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="800fa-161">Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="800fa-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="800fa-162">Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä</span><span class="sxs-lookup"><span data-stu-id="800fa-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="800fa-163">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin</span><span class="sxs-lookup"><span data-stu-id="800fa-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

