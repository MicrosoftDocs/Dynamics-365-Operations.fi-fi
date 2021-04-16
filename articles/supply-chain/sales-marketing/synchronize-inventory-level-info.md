---
title: Varastotasotietojen synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varastotasotiedot synkronoidaan Dynamics 365 Field Serviceen.
author: ChristianRytt
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c0db0c143abb8ce26a4a3007845050e4ddb02363
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840578"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="73efc-103">Varastotasotietojen synkronointi Supply Chain Managementista Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="73efc-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="73efc-104">Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Supply Chain Managementin varastotasotiedot synkronoidaan Dynamics 365 Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="73efc-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="73efc-105">[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="73efc-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="73efc-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="73efc-106">Templates and tasks</span></span>
<span data-ttu-id="73efc-107">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa käsillä olevia varastotasoja Supply Chain Managementista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="73efc-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="73efc-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="73efc-108">**Template in Data integration**</span></span>
- <span data-ttu-id="73efc-109">Tuotevarasto (Supply Chain Managementista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="73efc-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="73efc-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="73efc-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="73efc-111">Tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="73efc-111">Product inventory</span></span>

<span data-ttu-id="73efc-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin varastotasot voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="73efc-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="73efc-113">Varastot (Supply Chain Managementista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="73efc-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="73efc-114">Field Service -tuotteet, joissa varastoyksikkö (Supply Chain Managementista Salesiin)</span><span class="sxs-lookup"><span data-stu-id="73efc-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="73efc-115">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="73efc-115">Entity set</span></span>

| <span data-ttu-id="73efc-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="73efc-116">Field Service</span></span>                      | <span data-ttu-id="73efc-117">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="73efc-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="73efc-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="73efc-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="73efc-119">Dataversen käytettävissä oleva varasto varaston mukaan</span><span class="sxs-lookup"><span data-stu-id="73efc-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="73efc-120">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="73efc-120">Entity flow</span></span>
<span data-ttu-id="73efc-121">Valittujen tuotteiden varastotasotiedot lähetetään Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="73efc-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="73efc-122">Varastotasotietoja ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="73efc-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="73efc-123">Varastosaldo (tämän hetkinen kirjattu varastossa fyysisesti sijaitseva määrä)</span><span class="sxs-lookup"><span data-stu-id="73efc-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="73efc-124">Tilauksessa oleva määrä (tilauksessa oleva kirjattu kokonaismäärä, kuten myyntitilaukset)</span><span class="sxs-lookup"><span data-stu-id="73efc-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="73efc-125">Tilattu määrä (tilattu kirjattu kokonaismäärä, kuten ostotilaukset)</span><span class="sxs-lookup"><span data-stu-id="73efc-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="73efc-126">Nämä tiedot tallennetaan kullekin vapautetulle tuotteelle jokaisessa varastossa. Lisäksi ne synkronoidaan muutosten seurannan perusteella, kun varastotaso muuttuu.</span><span class="sxs-lookup"><span data-stu-id="73efc-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="73efc-127">Field Servicessa integrointiratkaisu luo muutokselle varastokirjauskansiot, jotta Field Servicen tasot saadaan vastaamaan Supply Chain Managementin tasoja.</span><span class="sxs-lookup"><span data-stu-id="73efc-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="73efc-128">Supply Chain Management toimii päävarastotasona.</span><span class="sxs-lookup"><span data-stu-id="73efc-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="73efc-129">Tämän vuoksi on tärkeää, että työtilausten, siirtojen ja oikaisujen integrointi Field Servicesta Supply Chain Managementiin määritetään, jos tätä toimintoa käytetään Field Servicessa yhdessä Supply Chain Managementin varastotasojen synkronoinnin kanssa.</span><span class="sxs-lookup"><span data-stu-id="73efc-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="73efc-130">Jos tuotteiden ja varastojen varastotasoja hallitaan Supply Chain Managementista, niitä voidaan hallita kyselyn ja suodatuksen lisäasetuksilla (Power Query).</span><span class="sxs-lookup"><span data-stu-id="73efc-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="73efc-131">Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti = Ei**) ja ne voi sitten yhdistää yhteen varastoon Supply Chain Managementissa kyselyn ja suodatuksen lisäasetustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="73efc-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="73efc-132">Tämä menettelyä käytetään tilanteissa, joissa Field Servicella halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="73efc-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="73efc-133">Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Supply Chain Managementista.</span><span class="sxs-lookup"><span data-stu-id="73efc-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="73efc-134">Lisätietoja on kohdissa [Varasto-oikaisujen synkronointi Field Servicesta Supply Chain Managementiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin linkitettyihin myyntitilauksiin Supply Chain Managementissa](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="73efc-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="73efc-135">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="73efc-135">Field Service CRM solution</span></span>
<span data-ttu-id="73efc-136">Uutta **Ulkoinen tuotevarasto** -yksikköä käytetään integroinnissa vain taustatoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="73efc-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="73efc-137">Tämä entiteetti vastaanottaa integroinnissa varastotasoarvot Supply Chain Managementista ja muuntaa sitten nämä arvot manuaalisiksi varastokirjauskansioksi, joka puolestaan muuttaa varastotuotteet varastossa.</span><span class="sxs-lookup"><span data-stu-id="73efc-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="73efc-138">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="73efc-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="73efc-139">Tietojen integrointi</span><span class="sxs-lookup"><span data-stu-id="73efc-139">Data integration</span></span>
<span data-ttu-id="73efc-140">Jotta projekti toimisi, on varmistettava, että integrointiavain päivitetään msdynce_externalproductinventories-mallia varten.</span><span class="sxs-lookup"><span data-stu-id="73efc-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="73efc-141">Siirry **Tietojen integrointi > Yhteysjoukot**.</span><span class="sxs-lookup"><span data-stu-id="73efc-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="73efc-142">Valitse käytetty yhteysjoukko.</span><span class="sxs-lookup"><span data-stu-id="73efc-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="73efc-143">Varmista, että **Integroinnin avain** -välilehdessä seuraavat avaimet lisätään msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="73efc-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="73efc-144">msdynce_productnumber (Product Number)</span><span class="sxs-lookup"><span data-stu-id="73efc-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="73efc-145">msdynce_warehouseid (Warehouse ID)</span><span class="sxs-lookup"><span data-stu-id="73efc-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="73efc-146">Tietojen integrointiprojekti</span><span class="sxs-lookup"><span data-stu-id="73efc-146">Data integration project</span></span>
<span data-ttu-id="73efc-147">Voit käyttää kyselyn ja suodatuksen lisäasetusten suodattimia siten, että vain tietyt tuotteet ja varastot lähettävät varastotasotietoja Supply Chain Managementista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="73efc-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="73efc-148">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="73efc-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="73efc-149">Tuotevarasto (Supply Chain Managementista Field Serviceen): Tuotevarasto</span><span class="sxs-lookup"><span data-stu-id="73efc-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="73efc-150">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="73efc-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]