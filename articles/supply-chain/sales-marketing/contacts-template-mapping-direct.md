---
title: Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin
description: Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -yksiköt synkronoidaan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994041"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="32078-103">Salesin yhteyshenkilöiden synkronointi suoraan Supply Chain Managementin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="32078-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="32078-104">Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](https://docs.microsoft.com/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="32078-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="32078-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Yhteyshenkilö (yhteyshenkilöt)- ja Yhteyshenkilöt (asiakkaat) -taulut synkronoidaan suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="32078-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="32078-106">Prospektista käteiseksi -ratkaisun tiedonkulku</span><span class="sxs-lookup"><span data-stu-id="32078-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="32078-107">Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa.</span><span class="sxs-lookup"><span data-stu-id="32078-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="32078-108">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="32078-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="32078-109">Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="32078-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="32078-110">[![Prospektista käteiseksi -ratkaisun tiedonkulku](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="32078-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="32078-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="32078-111">Templates and tasks</span></span>

<span data-ttu-id="32078-112">Näet käytettävissä olevat mallit avaamalla [PowerApps-hallintakeskuksen](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="32078-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="32078-113">Valitse **Projektit** ja valitse sitten julkisia malleja oikeassa yläkulmassa olevan **Uusi projekti** -kohdan avulla.</span><span class="sxs-lookup"><span data-stu-id="32078-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="32078-114">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin Yhteyshenkilö (Yhteyshenkilöt) -taulut Supply Chain Managementin Yhteyshenkilö (Asiakkaat) -tauluun.</span><span class="sxs-lookup"><span data-stu-id="32078-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="32078-115">**Mallien nimet tietojen integroinnissa**</span><span class="sxs-lookup"><span data-stu-id="32078-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="32078-116">Yhteyshenkilöt (Salesista Supply Chain Managementiin) – suora</span><span class="sxs-lookup"><span data-stu-id="32078-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="32078-117">Yhteyshenkilöistä asiakkaaseen (Salesista Supply Chain Managementiin) - suora</span><span class="sxs-lookup"><span data-stu-id="32078-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="32078-118">**Tietojen integrointiprojektin tehtävien nimet**</span><span class="sxs-lookup"><span data-stu-id="32078-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="32078-119">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="32078-119">Contacts</span></span>
    - <span data-ttu-id="32078-120">Yhteyshenkilö asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="32078-120">ContactToCustomer</span></span>

<span data-ttu-id="32078-121">Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="32078-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="32078-122">Yksikköjoukot</span><span class="sxs-lookup"><span data-stu-id="32078-122">Entity sets</span></span>

| <span data-ttu-id="32078-123">Myynti</span><span class="sxs-lookup"><span data-stu-id="32078-123">Sales</span></span>    | <span data-ttu-id="32078-124">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="32078-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="32078-125">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="32078-125">Contacts</span></span> | <span data-ttu-id="32078-126">Dataversen yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="32078-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="32078-127">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="32078-127">Contacts</span></span> | <span data-ttu-id="32078-128">Asiakkaat V2</span><span class="sxs-lookup"><span data-stu-id="32078-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="32078-129">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="32078-129">Entity flow</span></span>

<span data-ttu-id="32078-130">Yhteyshenkilöitä hallitaan Salesista ja synkronoidaan Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="32078-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="32078-131">Salesin yhteyshenkilöstä voi tulla Supply Chain Managementin yhteyshenkilö tai asiakas.</span><span class="sxs-lookup"><span data-stu-id="32078-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="32078-132">Järjestelmä etsii Salesista seuraavat ominaisuudet ja määrittää synkronoidaanko Salesin yhteyshenkilö Supply Chain Managementiin yhteyshenkilönä vai asiakkaana:</span><span class="sxs-lookup"><span data-stu-id="32078-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="32078-133">**Synkronointi Supply Chain Managementin asiakkaaseen:** yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="32078-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="32078-134">**Synkronointi Supply Chain Managementin yhteyshenkilöön:** Yhteyshenkilöt, joiden **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai yhteyshenkilö) viittaa tiliin (eikä yhteyshenkilöön)</span><span class="sxs-lookup"><span data-stu-id="32078-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="32078-135">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="32078-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="32078-136">Uusi **On aktiivinen asiakas** -sarake on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="32078-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="32078-137">Tämän sarakkeen avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole.</span><span class="sxs-lookup"><span data-stu-id="32078-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="32078-138">**On aktiivinen asiakas** -asetuksena on **Kyllä** vain yhteyshenkilöille, joilla on liittyviä tarjouksia, tilauksia tai laskuja.</span><span class="sxs-lookup"><span data-stu-id="32078-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="32078-139">Vain nämä yhteyshenkilöt synkronoidaan Supply Chain Managementiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="32078-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="32078-140">Uusi **IsCompanyAnAccount**-sarake on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="32078-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="32078-141">Tämä sarake osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö).</span><span class="sxs-lookup"><span data-stu-id="32078-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="32078-142">Näillä tiedoilla tunnistetaan yhteyshenkilöt, jotka on synkronoitava Supply Chain Managementiin yhteyshenkilöinä.</span><span class="sxs-lookup"><span data-stu-id="32078-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="32078-143">Uusi **Yhteyshenkilön numero** -sarake on lisätty yhteyshenkilöön, jotta integroinnin luonnollinen ja yksilöllinen avain voidaan taata.</span><span class="sxs-lookup"><span data-stu-id="32078-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="32078-144">Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="32078-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="32078-145">Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="32078-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="32078-146">Esimerkki: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="32078-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="32078-147">Kun Salesin integrointiratkaisu otetaan käyttöön, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -sarakkeen käyttämällä edellä mainittua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="32078-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="32078-148">Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -sarakkeen arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.</span><span class="sxs-lookup"><span data-stu-id="32078-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="32078-149">Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="32078-149">In Supply Chain Management</span></span>

<span data-ttu-id="32078-150">Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="32078-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="32078-151">Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="32078-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="32078-152">Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.</span><span class="sxs-lookup"><span data-stu-id="32078-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="32078-153">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="32078-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="32078-154">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="32078-154">Contact to customer</span></span>

- <span data-ttu-id="32078-155">**CustomerGroup** on pakollinen Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="32078-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="32078-156">Voit estää synkronointivirheet määrittämällä yhdistämismäärityksen oletusarvon.</span><span class="sxs-lookup"><span data-stu-id="32078-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="32078-157">Oletusarvoa käytetään, jos sarake on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="32078-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="32078-158">Oletusmallin arvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="32078-158">The default template value is **10**.</span></span>

- <span data-ttu-id="32078-159">Kun seuraavat yhdistämismääritykset lisätään, Supply Chain Managementissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="32078-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="32078-160">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="32078-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="32078-161">**SiteId** – oletustoimipaikka voidaan määrittää myös Supply Chain Managementin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="32078-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="32078-162">Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="32078-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="32078-163">Mallin **SiteId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="32078-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="32078-164">**WarehouseId** – Oletusvarasto voidaan määrittää myös Supply Chain Managementin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="32078-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="32078-165">Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="32078-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="32078-166">Mallin **WarehouseId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="32078-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="32078-167">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="32078-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="32078-168">Oletusmallin arvo on **fi-fi**.</span><span class="sxs-lookup"><span data-stu-id="32078-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="32078-169">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="32078-169">Template mapping in Data integration</span></span>

<span data-ttu-id="32078-170">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="32078-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="32078-171">Yhdistämismääritys osoittaa, minkä sarakkeen tiedot synkronoidaan Salesista Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="32078-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="32078-172">Yhteyshenkilöstä yhteyshenkilöön</span><span class="sxs-lookup"><span data-stu-id="32078-172">Contact to contact</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="32078-174">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="32078-174">Contact to customer</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="32078-176">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="32078-176">Related topics</span></span>

[<span data-ttu-id="32078-177">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="32078-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="32078-178">Tilien synkronointi suoraan Salesin tuotteista Supply Chain Managementin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="32078-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="32078-179">Supply Chain Managementin tuotteiden synkronointi suoraan Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="32078-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="32078-180">Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä</span><span class="sxs-lookup"><span data-stu-id="32078-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="32078-181">Myyntilaskujen otsikoiden ja rivien synkronointi suoraan Supply Chain Managementista Salesiin</span><span class="sxs-lookup"><span data-stu-id="32078-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


