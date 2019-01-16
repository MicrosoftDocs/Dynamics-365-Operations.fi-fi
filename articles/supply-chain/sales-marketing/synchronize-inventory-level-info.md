---
title: Finance and Operationsin varastotasotietojen synkronointi Field Serviceen
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e302f-103">Finance and Operationsin varastotasotietojen synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="e302f-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e302f-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="e302f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e302f-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e302f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e302f-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="e302f-106">Templates and tasks</span></span>
<span data-ttu-id="e302f-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin käsillä olevat varastotasot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="e302f-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e302f-108">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="e302f-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e302f-109">Tuotevarasto (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="e302f-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="e302f-110">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="e302f-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e302f-111">Tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="e302f-111">Product inventory</span></span>

<span data-ttu-id="e302f-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="e302f-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e302f-113">Varastot (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="e302f-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="e302f-114">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="e302f-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e302f-115">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="e302f-115">Entity set</span></span>

| <span data-ttu-id="e302f-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e302f-116">Field Service</span></span>                      | <span data-ttu-id="e302f-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e302f-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e302f-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e302f-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e302f-119">Käytettävissä oleva CDS-varasto varaston mukaan</span><span class="sxs-lookup"><span data-stu-id="e302f-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e302f-120">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="e302f-120">Entity flow</span></span>
<span data-ttu-id="e302f-121">Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen-</span><span class="sxs-lookup"><span data-stu-id="e302f-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="e302f-122">Varastotasotietoja ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="e302f-122">The inventory level information include:</span></span> 
- <span data-ttu-id="e302f-123">Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)</span><span class="sxs-lookup"><span data-stu-id="e302f-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="e302f-124">Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä eli myyntitilaukset)</span><span class="sxs-lookup"><span data-stu-id="e302f-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="e302f-125">Tilattu määrä (tilattu kirjattu kokonaismäärä eli ostotilaukset)</span><span class="sxs-lookup"><span data-stu-id="e302f-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="e302f-126">Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.</span><span class="sxs-lookup"><span data-stu-id="e302f-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e302f-127">Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Finance and Operationsin tasoja.</span><span class="sxs-lookup"><span data-stu-id="e302f-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e302f-128">Finance and Operations toimii päävarastotasona.</span><span class="sxs-lookup"><span data-stu-id="e302f-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e302f-129">Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicestä Finance and Operationsiin määritetään, jos tätä toimintoa käytetään Field Servicessä yhdessä Finance and Operationsin varastotasojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="e302f-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e302f-130">Jos tuotteiden ja varastojen varastotasoja hallitaan Finance and Operationsista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).</span><span class="sxs-lookup"><span data-stu-id="e302f-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="e302f-131">Huomautus: Field Servicessä voi luoda useita varastoja (kun On ulkoisesti ylläpidetty = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="e302f-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e302f-132">Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="e302f-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e302f-133">Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="e302f-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e302f-134">Lisätietoja on kohdissa Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin ja Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="e302f-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e302f-135">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="e302f-135">Field Service CRM solution</span></span>
<span data-ttu-id="e302f-136">Ulkoinen tuotevarasto -yksikkö on uusi yksikkö, jota käytetään integroinnissa vain taustatoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="e302f-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="e302f-137">Se vastaanottaa integroinnissa varastotasoarvot Finance and Operationsista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa.</span><span class="sxs-lookup"><span data-stu-id="e302f-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e302f-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="e302f-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="e302f-139">Tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="e302f-139">In the Data Integration project</span></span>
<span data-ttu-id="e302f-140">Voit määrittää kyselyn ja suodatuksen lisäasetusten suodattimilla, että vain valitut tuotteet ja varastot lähettävät varastotasotietoja Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="e302f-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e302f-141">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="e302f-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="e302f-142">Tuotevarasto (Finance and Operationsista Field Serviceen): tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="e302f-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="e302f-143">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e302f-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

