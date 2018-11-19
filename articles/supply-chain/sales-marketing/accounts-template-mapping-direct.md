---
title: Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Sales -tilit synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: a0cabdab63d4d44010e52303d6f487db1e910059
ms.contentlocale: fi-fi
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="97fdb-103">Salesin asiakkaiden synkronointi suoraan Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="97fdb-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="97fdb-104">Tutustu [sovellusten Common Data Servicen tietojen integrointiin](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="97fdb-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="97fdb-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Sales -tilit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="97fdb-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="97fdb-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="97fdb-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="97fdb-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="97fdb-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="97fdb-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="97fdb-109">Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="97fdb-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="97fdb-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="97fdb-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="97fdb-111">Templates and tasks</span></span>

<span data-ttu-id="97fdb-112">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="97fdb-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="97fdb-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="97fdb-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="97fdb-114">Seuraava mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan tilit Sales-sovelluksesta Finance and Operations -sovellukseen:</span><span class="sxs-lookup"><span data-stu-id="97fdb-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="97fdb-115">**Mallin nimi tietojen integroinnissa:** tilit (Salesista Fin and Opsiin) – suora</span><span class="sxs-lookup"><span data-stu-id="97fdb-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="97fdb-116">**Projektin tehtävän nimi:** tilit – asiakkaat</span><span class="sxs-lookup"><span data-stu-id="97fdb-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="97fdb-117">Synkronointitehtävät on suoritettava, ennen kuin tilin ja asiakkaan synkronointi on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="97fdb-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="97fdb-118">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="97fdb-118">Entity set</span></span>

| <span data-ttu-id="97fdb-119">Myynti</span><span class="sxs-lookup"><span data-stu-id="97fdb-119">Sales</span></span>    | <span data-ttu-id="97fdb-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97fdb-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="97fdb-121">Tilit</span><span class="sxs-lookup"><span data-stu-id="97fdb-121">Accounts</span></span> | <span data-ttu-id="97fdb-122">Asiakkaat V2</span><span class="sxs-lookup"><span data-stu-id="97fdb-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="97fdb-123">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="97fdb-123">Entity flow</span></span>

<span data-ttu-id="97fdb-124">Summia hallitaan Salesissa ja synkronoidaan Finance and Operationsiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="97fdb-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="97fdb-125">Näiden asiakkaiden **On ulkoisesti ylläpidetty** -ominaisuuden arvoksi on määritetty **Kyllä**, jotta Salesista peräisin olevia asiakkaita voidaan jäljittää.</span><span class="sxs-lookup"><span data-stu-id="97fdb-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="97fdb-126">Näitä tietoja käytetään suodattamaan Salesiin synkronoitavat laskut laskutuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="97fdb-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="97fdb-127">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="97fdb-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="97fdb-128">**Tilinumero**-kenttä on käytettävissä **Tili**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="97fdb-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="97fdb-129">Se on nyt luontainen ja yksilöllinen avain, joka tukee integrointia.</span><span class="sxs-lookup"><span data-stu-id="97fdb-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="97fdb-130">Asiakkuudenhallinta- eli CRM-ratkaisun luonnollinen avain -ominaisuudella voi olla vaikutusta asiakkaisiin, jotka käyttävät jo **Tilinumero**-kenttää mutta eivät yksilöllisiä tilikohtaisia **Tilinumero**-arvoja.</span><span class="sxs-lookup"><span data-stu-id="97fdb-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="97fdb-131">Integrointiratkaisu ei tue tätä tapausta tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="97fdb-132">Jos **Tilinumero**-arvoa ei ole vielä luotu, kun uusi tili luodaan, se luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="97fdb-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="97fdb-133">Arvossa on ensimmäisenä **ACC**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="97fdb-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="97fdb-134">Esimerkki: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="97fdb-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="97fdb-135">Kun Salesin integrointiratkaisua käytetään, päivityskomentosarja määrittää aiemmin Salesissa luotujen tilien **Tilinumero**-kentän.</span><span class="sxs-lookup"><span data-stu-id="97fdb-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="97fdb-136">Jos **Tilinumero**-arvoja ei ole, käytetään edellä mainittua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="97fdb-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="97fdb-137">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="97fdb-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="97fdb-138">**CustomerGroupId**-yhdistämismääritys on päivitettävä Finance and Operationsin kelvolliseksi arvoksi.</span><span class="sxs-lookup"><span data-stu-id="97fdb-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="97fdb-139">Voit määrittää oletusarvon. Vaihtoehtoisesti voit määrittää arvon arvomäärityksellä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="97fdb-140">Oletusmallin arvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="97fdb-140">The default template value is **10**.</span></span>

- <span data-ttu-id="97fdb-141">Kun seuraavat yhdistämismääritykset lisätään, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="97fdb-142">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="97fdb-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="97fdb-143">**SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="97fdb-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="97fdb-144">Oletustoimipaikka voidaan ottaa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="97fdb-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="97fdb-145">Oletusmallin arvo on **1**.</span><span class="sxs-lookup"><span data-stu-id="97fdb-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="97fdb-146">**WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="97fdb-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="97fdb-147">Oletusvarasto voidaan ottaa Finance and Operationsissa joko tuotteesta tai tilauksen otsikossa olevasta asiakkaasta.</span><span class="sxs-lookup"><span data-stu-id="97fdb-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="97fdb-148">Oletusmallin arvo on **13**.</span><span class="sxs-lookup"><span data-stu-id="97fdb-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="97fdb-149">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="97fdb-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="97fdb-150">Oletusarvoisesti käytetään asiakkaan tilausotsikon kieltä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="97fdb-151">Oletusmallin arvo on **fi-fi**.</span><span class="sxs-lookup"><span data-stu-id="97fdb-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="97fdb-152">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="97fdb-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="97fdb-153">**Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="97fdb-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="97fdb-154">Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="97fdb-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="97fdb-155">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="97fdb-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="97fdb-156">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="97fdb-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="97fdb-158">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="97fdb-158">Related topics</span></span>


[<span data-ttu-id="97fdb-159">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="97fdb-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="97fdb-160">Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="97fdb-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="97fdb-161">Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="97fdb-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="97fdb-162">Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="97fdb-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="97fdb-163">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="97fdb-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


