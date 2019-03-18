---
title: Finance and Operationsin varastotasotietojen synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "356780"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="ac3f5-103">Finance and Operationsin varastotasotietojen synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="ac3f5-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac3f5-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Finance and Operationsin varastotasotiedot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ac3f5-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ac3f5-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="ac3f5-106">Templates and tasks</span></span>
<span data-ttu-id="ac3f5-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin käsillä olevat varastotasot synkronoidaan Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ac3f5-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="ac3f5-108">**Template in Data integration**</span></span>
- <span data-ttu-id="ac3f5-109">Tuotevarasto (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="ac3f5-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="ac3f5-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="ac3f5-111">Tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="ac3f5-111">Product inventory</span></span>

<span data-ttu-id="ac3f5-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="ac3f5-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="ac3f5-113">Varastot (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="ac3f5-114">Field Service -tuotteet, joissa varastoyksikkö (Finance and Operationsista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-114">Field Service products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="ac3f5-115">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="ac3f5-115">Entity set</span></span>

| <span data-ttu-id="ac3f5-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="ac3f5-116">Field Service</span></span>                      | <span data-ttu-id="ac3f5-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac3f5-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="ac3f5-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="ac3f5-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="ac3f5-119">Käytettävissä oleva CDS-varasto varaston mukaan</span><span class="sxs-lookup"><span data-stu-id="ac3f5-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="ac3f5-120">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="ac3f5-120">Entity flow</span></span>
<span data-ttu-id="ac3f5-121">Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="ac3f5-122">Varastotasotietoja ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="ac3f5-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="ac3f5-123">Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="ac3f5-124">Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä, kuten myyntitilaukset)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="ac3f5-125">Tilattu määrä (tilattu kirjattu kokonaismäärä, kuten ostotilaukset)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="ac3f5-126">Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="ac3f5-127">Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Finance and Operationsin tasoja.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="ac3f5-128">Finance and Operations toimii päävarastotasona.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="ac3f5-129">Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicestä Finance and Operationsiin määritetään, jos tätä toimintoa käytetään Field Servicessä yhdessä Finance and Operationsin varastotasojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="ac3f5-130">Jos tuotteiden ja varastojen varastotasoja hallitaan Finance and Operationsista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).</span><span class="sxs-lookup"><span data-stu-id="ac3f5-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="ac3f5-131">Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti = Ei**) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="ac3f5-132">Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="ac3f5-133">Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="ac3f5-134">Lisätietoja on kohdissa [Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="ac3f5-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ac3f5-135">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ac3f5-135">Field Service CRM solution</span></span>
<span data-ttu-id="ac3f5-136">Uutta **Ulkoinen tuotevarasto** -yksikköä käytetään integroinnissa vain taustatoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="ac3f5-137">Tämä entiteetti vastaanottaa integroinnissa varastotasoarvot Finance and Operationsista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ac3f5-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="ac3f5-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="ac3f5-139">Tietojen integrointiprojekti</span><span class="sxs-lookup"><span data-stu-id="ac3f5-139">Data integration project</span></span>
<span data-ttu-id="ac3f5-140">Voit käyttää kyselyn ja suodatuksen lisäasetusten suodattimia siten, että vain tietyt tuotteet ja varastot lähettävät varastotasotietoja Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="ac3f5-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ac3f5-141">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ac3f5-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="ac3f5-142">Tuotevarasto (Finance and Operationsista Field Serviceen): tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="ac3f5-142">Product inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="ac3f5-143">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="ac3f5-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>