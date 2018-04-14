---
title: "Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin"
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d0da8d3f854fe05db2f73d080ec699d0bedfcdb5
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="43e42-103">Salesin yhteyshenkilöiden synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="43e42-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="43e42-104">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="43e42-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="43e42-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="43e42-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="43e42-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="43e42-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="43e42-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Finance and Operations and Sales -esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="43e42-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="43e42-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="43e42-109">Seuraavassa kuvassa kerrotaan, miten tiedot synkronoidaan Finance and Operations- ja Sales-sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="43e42-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="43e42-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="43e42-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43e42-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="43e42-111">Templates and tasks</span></span>

<span data-ttu-id="43e42-112">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="43e42-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="43e42-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="43e42-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="43e42-114">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin yhteyshenkilön (yhteyshenkilöt) yksiköt Finance and Operationsin yhteyshenkilön (asiakkaat) yksikköön:</span><span class="sxs-lookup"><span data-stu-id="43e42-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="43e42-115">**Mallien nimet tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="43e42-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="43e42-116">Yhteyshenkilöt (Salesista Fin and Opsiin) - suora</span><span class="sxs-lookup"><span data-stu-id="43e42-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="43e42-117">Yhteyshenkilöistä asiakkaaseen (Salesista Fin and Opsiin) - suora</span><span class="sxs-lookup"><span data-stu-id="43e42-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="43e42-118">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="43e42-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="43e42-119">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="43e42-119">Contacts</span></span>
    - <span data-ttu-id="43e42-120">Yhteyshenkilö asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="43e42-120">ContactToCustomer</span></span>

<span data-ttu-id="43e42-121">Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="43e42-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="43e42-122">Yksikköjoukot</span><span class="sxs-lookup"><span data-stu-id="43e42-122">Entity sets</span></span>

| <span data-ttu-id="43e42-123">Myynti</span><span class="sxs-lookup"><span data-stu-id="43e42-123">Sales</span></span>    | <span data-ttu-id="43e42-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43e42-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="43e42-125">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="43e42-125">Contacts</span></span> | <span data-ttu-id="43e42-126">CDS-yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="43e42-126">CDS Contacts</span></span>           |
| <span data-ttu-id="43e42-127">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="43e42-127">Contacts</span></span> | <span data-ttu-id="43e42-128">Asiakkaat V2</span><span class="sxs-lookup"><span data-stu-id="43e42-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="43e42-129">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="43e42-129">Entity flow</span></span>

<span data-ttu-id="43e42-130">Yhteyshenkilöitä hallitaan Salesissa ja ne synkronoidaan Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="43e42-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="43e42-131">Salesin yhteyshenkilöstä voi tulla Finance and Operationsin yhteyshenkilö tai asiakas.</span><span class="sxs-lookup"><span data-stu-id="43e42-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="43e42-132">Järjestelmä etsii Sales-sovelluksesta seuraavat ominaisuudet ja määrittää synkronoidaanko Salesin yhteyshenkilö Finance and Operationsiin yhteyshenkilönä vai asiakkaana:</span><span class="sxs-lookup"><span data-stu-id="43e42-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="43e42-133">**Synkronointi asiakkaaksi Finance and Operationsissa:** yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="43e42-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="43e42-134">**Synkronointi yhteyshenkilöksi Finance and Operationsissa:** Yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai asiakas) viittaa tiliin (eikä yhteyshenkilöön)</span><span class="sxs-lookup"><span data-stu-id="43e42-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="43e42-135">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="43e42-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="43e42-136">Uusi **On aktiivinen asiakas** -kenttä on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="43e42-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="43e42-137">Tämän kentän avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole.</span><span class="sxs-lookup"><span data-stu-id="43e42-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="43e42-138">**On aktiivinen asiakas** -asetuksena on **Kyllä** vain yhteyshenkilöille, joilla on liittyviä tarjouksia, tilauksia tai laskuja.</span><span class="sxs-lookup"><span data-stu-id="43e42-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="43e42-139">Vain nämä yhteyshenkilöt synkronoidaan Finance and Operationsiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="43e42-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="43e42-140">Uusi **IsCompanyAnAccount**-kenttä on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="43e42-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="43e42-141">Tämä kenttä osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö).</span><span class="sxs-lookup"><span data-stu-id="43e42-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="43e42-142">Näillä tiedoilla tunnistetaan yhteyshenkilöt, jotka on synkronoitava Finance and Operationsiin yhteyshenkilöinä.</span><span class="sxs-lookup"><span data-stu-id="43e42-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="43e42-143">Uusi **Yhteyshenkilön numero** -kenttä on lisätty yhteyshenkilöön, jotta integroinnin luonnollinen ja yksilöllinen avain voidaan taata.</span><span class="sxs-lookup"><span data-stu-id="43e42-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="43e42-144">Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="43e42-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="43e42-145">Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="43e42-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="43e42-146">Esimerkki: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="43e42-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="43e42-147">Kun Salesin integrointiratkaisu otetaan käyttöön, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -kentän käyttämällä edellä mainittua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="43e42-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="43e42-148">Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -kentän arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.</span><span class="sxs-lookup"><span data-stu-id="43e42-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="43e42-149">Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="43e42-149">In Finance and Operations</span></span>

<span data-ttu-id="43e42-150">Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="43e42-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="43e42-151">Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="43e42-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="43e42-152">Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="43e42-153">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="43e42-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="43e42-154">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="43e42-154">Contact to customer</span></span>

- <span data-ttu-id="43e42-155">**CustomerGroup** tarvitaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="43e42-156">Voit estää synkronointivirheet määrittämällä yhdistämismäärityksen oletusarvon.</span><span class="sxs-lookup"><span data-stu-id="43e42-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="43e42-157">Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="43e42-158">Oletusmallin arvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="43e42-158">The default template value is **10**.</span></span>

- <span data-ttu-id="43e42-159">Kun seuraavat yhdistämismääritykset lisätään, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="43e42-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="43e42-160">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="43e42-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="43e42-161">**SiteId** – oletustoimipaikka voidaan määrittää myös Finance and Operationsin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="43e42-162">Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="43e42-163">Mallin **SiteId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="43e42-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="43e42-164">**WarehouseId** – oletusvarasto voidaan määrittää myös Finance and Operationsin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="43e42-165">Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="43e42-166">Mallin **WarehouseId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="43e42-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="43e42-167">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="43e42-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="43e42-168">Oletusmallin arvo on **fi-fi**.</span><span class="sxs-lookup"><span data-stu-id="43e42-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43e42-169">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="43e42-169">Template mapping in Data integration</span></span>

<span data-ttu-id="43e42-170">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="43e42-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="43e42-171">Yhdistämismääritys osoittaa, minkä kentän tiedot synkronoidaan Salesista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="43e42-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="43e42-172">Yhteyshenkilöstä yhteyshenkilöön</span><span class="sxs-lookup"><span data-stu-id="43e42-172">Contact to contact</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="43e42-174">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="43e42-174">Contact to customer</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="43e42-176">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="43e42-176">Related topics</span></span>

[<span data-ttu-id="43e42-177">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="43e42-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="43e42-178">Sales-asiakkaiden synkronointi suoraan Finance and Operations -asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="43e42-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="43e42-179">Finance and Operationsin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="43e42-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="43e42-180">Myyntitilauksien otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="43e42-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="43e42-181">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="43e42-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



