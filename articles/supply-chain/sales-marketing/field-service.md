---
title: Microsoft Dynamics 365 Field Service -integroinnin yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Field Servicen integroinnista.
author: ChristianRytt
ms.date: 07/25/2019
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
ms.openlocfilehash: 73d20958d0efadefc709db524fe16ed85d1ea33a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824891"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="094f3-103">Microsoft Dynamics 365 Field Service -integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="094f3-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="094f3-104">Supply Chain Management mahdollistaa liiketoimintaprosessien synkronoinnin Dynamics 365 Supply Chain Managementin ja Dynamics 365 Field Servicen välillä</span><span class="sxs-lookup"><span data-stu-id="094f3-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="094f3-105">Integrointiskenaariot määritetään käyttämällä laajennettavia tietojen integrointitoiminnon malleja ja Microsoft Dataverse -palvelua. Niiden avulla liiketoimintaprosessien synkronointi voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="094f3-105">The integration scenarios are configured by using extensible Data integrator templates and Microsoft Dataverse to enable the synchronization of business processes.</span></span>
<span data-ttu-id="094f3-106">Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiosarakkeita ja mukautettuja sarakkeita ja taulukoita yhdistämällä voidaan muokata integrointi liiketoimintatarpeita vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="094f3-106">Standard templates can be used to create custom integration projects, where additional standard and custom columns and tables can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="094f3-107">Field Service -integrointi perustuu aiempaan myyntimahdollisuudesta maksutapahtumaan -toimintoon.</span><span class="sxs-lookup"><span data-stu-id="094f3-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/field-service-integration.png)

<span data-ttu-id="094f3-109">Field Servicen ja Supply Chain Managementin välisen integroinnin ensimmäinen vaihe keskittyy siihen, että Field Servicen työtilauksia ja sopimuksia voidaan laskuttaa Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="094f3-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="094f3-110">Tuettu työnkulku käynnistyy Field Servicessä, jossa työtilausten tiedot synkronoidaan Supply Chain Managementiin myyntitilauksina.</span><span class="sxs-lookup"><span data-stu-id="094f3-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="094f3-111">Supply Chain Managementissa myyntitilaukset laskutetaan, jotta laskuasiakirjat voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="094f3-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="094f3-112">Myös Field Servicen sopimuslaskujen tiedot synkronoidaan Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="094f3-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="094f3-113">Microsoft Dynamics 365:n tietojen integrointitoiminto synkronoi tiedot käyttämällä mukautettavia projekteja.</span><span class="sxs-lookup"><span data-stu-id="094f3-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="094f3-114">Mukautettujen integrointiprojektien luontiin voidaan käyttää vakiomalleja. Näissä projekteissa lisävakiosarakkeita ja mukautettuja sarakkeita sekä taulukoita yhdistämällä voidaan muokata integrointi tarpeita vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="094f3-114">Standard templates can be used to create custom integration projects where additional standard and custom columns, and also tables, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="094f3-115">Field Servicen ja Supply Chain Managementin ensimmäisen vaiheen integrointi mahdollistaa seuraavien nimikkeiden synkronoinnin:</span><span class="sxs-lookup"><span data-stu-id="094f3-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="094f3-116">Supply Chain Managementin tuotteiden synkronointi Field Servicen tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="094f3-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="094f3-117">Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin</span><span class="sxs-lookup"><span data-stu-id="094f3-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="094f3-118">Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin</span><span class="sxs-lookup"><span data-stu-id="094f3-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="094f3-119">Esimerkki työtilauksen synkronoimisesta Field Servicen ja Supply Chain Managementin välillä on lyhyessä YouTube-videossa [Työtilauksen synkronointi Microsoft Dynamics 365:n integroinnilla](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="094f3-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="094f3-120">Integrointi Field Servicen kanssa varasto- ja projektitiedot mukaan lukien</span><span class="sxs-lookup"><span data-stu-id="094f3-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="094f3-121">Tämä toisen vaiheen lisätoiminto keskittyi antamaan kenttätyöntekijöille käsityksen Supply Chain Managementin varastotiedoista, jotta he voivat päivittää varastotasot ja tehdä materiaalisiirtoja.</span><span class="sxs-lookup"><span data-stu-id="094f3-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="094f3-122">Lisäksi myytyjä hyödykkeitä asentavat tai huoltavat yritykset pystyvät hallitsemaan entistä paremmin koko myynti- ja huoltoprosessia sekä saavat paremman näkyvyyden tähän prosessiin projektien integroinnin ansiosta.</span><span class="sxs-lookup"><span data-stu-id="094f3-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="094f3-123">Toiminto sisältää seuraavien tietojen integroinnin:</span><span class="sxs-lookup"><span data-stu-id="094f3-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="094f3-124">Varastotiedot</span><span class="sxs-lookup"><span data-stu-id="094f3-124">Warehouse information</span></span>
- <span data-ttu-id="094f3-125">Käytettävissä olevan varaston tiedot</span><span class="sxs-lookup"><span data-stu-id="094f3-125">On-hand inventory information</span></span>
- <span data-ttu-id="094f3-126">Varastosiirrot</span><span class="sxs-lookup"><span data-stu-id="094f3-126">Inventory transfers</span></span>
- <span data-ttu-id="094f3-127">Varasto-oikaisut</span><span class="sxs-lookup"><span data-stu-id="094f3-127">Inventory adjustments</span></span>
- <span data-ttu-id="094f3-128">Supply Chain Management -projektit, jotka liittyvät Dynamics 365 Field Service -työtilauksiin</span><span class="sxs-lookup"><span data-stu-id="094f3-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="094f3-129">Dynamics 365 Field Servicen työtilaukset, joissa on linkki Supply Chain Management -projekteihin, käyttävät tätä projektinumeroa myyntitilauksessa, mikä mahdollistaa laskutuksen projektista.</span><span class="sxs-lookup"><span data-stu-id="094f3-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="094f3-131">Field Servicen ja Supply Chain Managementin toisen vaiheen integrointi mahdollistaa seuraavien mallien synkronoinnin:</span><span class="sxs-lookup"><span data-stu-id="094f3-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="094f3-132">Varastot (Supply Chain Managementista Field Serviceen) - varastot Supply Chain Managementista Field Serviceen [edistynyt kysely]</span><span class="sxs-lookup"><span data-stu-id="094f3-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="094f3-133">Tuotevarasto (Supply Chain Managementista Field Serviceen) - varastosaldotiedot Supply Chain Managementista Field Serviceen [edistynyt kysely]</span><span class="sxs-lookup"><span data-stu-id="094f3-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="094f3-134">Varastomuutos (Field Servicesta Supply Chain Managementiin) - Varaston muutokset Field Servicesta Supply Chain Managementiin [edistynyt kysely]</span><span class="sxs-lookup"><span data-stu-id="094f3-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="094f3-135">Varastosiirrot (Field Servicesta Supply Chain Managementiin) - Varaston siirrot Field Servicesta Supply Chain Managementiin [edistynyt kysely]</span><span class="sxs-lookup"><span data-stu-id="094f3-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="094f3-136">Projektit (Supply Chain Managementista Field Serviceen) - projektiluettelo Supply Chain Managementista Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="094f3-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="094f3-137">Projektin työtilaukset (Field Servicestä Supply Chain Managementiin) – Field Servicen työtilaukset Supply Chain Managementin myyntilauksiin ja projektituki [Lisäkysely]</span><span class="sxs-lookup"><span data-stu-id="094f3-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="094f3-138">Field Servicen tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin) – Supply Chain Managementin Myytävät vapautetut tuotteet Salesin Field Serviceen tuotteisiin, joissa varastoyksiköt</span><span class="sxs-lookup"><span data-stu-id="094f3-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="094f3-139">Järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="094f3-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="094f3-140">Supply Chain Managementin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="094f3-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="094f3-141">Field Servicen integrointi tukee seuraavia versioita:</span><span class="sxs-lookup"><span data-stu-id="094f3-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="094f3-142">Dynamics 365 for Finance and Operationsin versio 8.1.2 (joulukuu 2018) julkaistiin joulukuussa 2018; sen koontiversionumero on 8.1.195 ja Platform update 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="094f3-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="094f3-143">Field Servicen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="094f3-143">System requirements for Field Service</span></span>
<span data-ttu-id="094f3-144">Seuraavat komponentit on asennettava, jotta Field Service -integrointiratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="094f3-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="094f3-145">Field Service (versio 8.2.0.286) tai uusi versio Dynamics 365 9.1.x – julkaistiin marraskuussa 2018</span><span class="sxs-lookup"><span data-stu-id="094f3-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="094f3-146">Dynamics 365:N prospektista käteiseksi (P2C) -ratkaisu, versio 1.15.0.1 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="094f3-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="094f3-147">Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="094f3-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="094f3-148">Dynamics 365:n Field Servicen integrointi-, projekti- ja varastoratkaisu, versio 2.0.0.0 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="094f3-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="094f3-149">Ratkaisun voi ladata [AppSourcesta](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="094f3-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]