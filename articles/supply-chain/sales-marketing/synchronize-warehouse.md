---
title: Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835667"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="a63da-103">Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="a63da-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a63da-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla varastoja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="a63da-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a63da-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="a63da-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a63da-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="a63da-106">Templates and tasks</span></span>
<span data-ttu-id="a63da-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin fyysiset varastot Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="a63da-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a63da-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="a63da-108">**Template in Data integration**</span></span>
- <span data-ttu-id="a63da-109">Varastot (Fin and Opsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="a63da-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="a63da-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="a63da-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="a63da-111">Varasto</span><span class="sxs-lookup"><span data-stu-id="a63da-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="a63da-112">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="a63da-112">Entity set</span></span>
| <span data-ttu-id="a63da-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="a63da-113">Field Service</span></span>    | <span data-ttu-id="a63da-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a63da-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="a63da-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="a63da-115">msdyn_warehouses</span></span> | <span data-ttu-id="a63da-116">Varastot</span><span class="sxs-lookup"><span data-stu-id="a63da-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="a63da-117">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="a63da-117">Entity flow</span></span>
<span data-ttu-id="a63da-118">Finance and Operationsissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Common Data Servicen (CDS) tietojen integrointiprojektilla.</span><span class="sxs-lookup"><span data-stu-id="a63da-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="a63da-119">Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla.</span><span class="sxs-lookup"><span data-stu-id="a63da-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="a63da-120">Finance and Operationsista synkronoitavat fyysiset varastot luodaan Field Servicessä siten, että **Ylläpidetään ulkoisesti** -kentän asetukseksi määritetään **Kyllä**. Lisäksi tietue on vain luku -muotoinen.</span><span class="sxs-lookup"><span data-stu-id="a63da-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a63da-121">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a63da-121">Field Service CRM solution</span></span>
<span data-ttu-id="a63da-122">Field Servicen ja Finance and Operationsin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto.</span><span class="sxs-lookup"><span data-stu-id="a63da-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="a63da-123">**Ylläpidetään ulkoisesti** -kenttä on lisätty ratkaisussa **Varasto (msdyn_warehouses)** -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="a63da-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="a63da-124">Tämä kenttä auttaa määrittämään, käsitelläänkö varastoa Finance and Operationsista vai onko se vain Field Servicessä.</span><span class="sxs-lookup"><span data-stu-id="a63da-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="a63da-125">Tässä kentässä on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="a63da-125">The settings for this field include:</span></span>
- <span data-ttu-id="a63da-126">**Kyllä** – varasto on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.</span><span class="sxs-lookup"><span data-stu-id="a63da-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="a63da-127">**Ei** – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.</span><span class="sxs-lookup"><span data-stu-id="a63da-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="a63da-128">**Ylläpidetään ulkoisesti** -kenttä auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="a63da-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="a63da-129">Vain varastoja, joiden **Ylläpidetään ulkoisesti** -asetuksena on **Kyllä**, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="a63da-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="a63da-130">Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="a63da-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="a63da-131">Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a63da-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="a63da-132">Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="a63da-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="a63da-133">Lisätietoja on kohdissa [Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="a63da-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a63da-134">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="a63da-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="a63da-135">Tietojen integrointiprojekti</span><span class="sxs-lookup"><span data-stu-id="a63da-135">Data Integration project</span></span>
<span data-ttu-id="a63da-136">Ennen varastojen synkronointia projektin kyselyn ja suodatuksen lisäasetukset on päivitettävä sisältämään vain varastot, jotka haluat tuoda Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="a63da-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="a63da-137">Huomaa, että Field Servicen varasto tarvitaan, jotta sitä voidaan käyttää työtilauksissa, oikaisuissa ja siirroissa.</span><span class="sxs-lookup"><span data-stu-id="a63da-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="a63da-138">**msdyn_warehouses**-kohteen **integrointiavaimen** varmistaminen:</span><span class="sxs-lookup"><span data-stu-id="a63da-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="a63da-139">Siirry tietojen integrointiin.</span><span class="sxs-lookup"><span data-stu-id="a63da-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="a63da-140">Valitse **Yhteysjoukko**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a63da-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="a63da-141">Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="a63da-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="a63da-142">Valitse **Integrointiavain**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a63da-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="a63da-143">Etsi msdyn_warehouses ja varmista, että avain **msdyn_name (nimi)** on lisätty.</span><span class="sxs-lookup"><span data-stu-id="a63da-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="a63da-144">Jos avainta ei näy, lisää se valitsemalla ensin **Lisää avain** ja sitten **Tallenna** sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="a63da-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a63da-145">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="a63da-145">Template mapping in Data integration</span></span>

<span data-ttu-id="a63da-146">Seuraavassa kuvassa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a63da-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="a63da-147">Varastot (Fin and Opsista Field Serviceen): Varasto</span><span class="sxs-lookup"><span data-stu-id="a63da-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="a63da-148">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="a63da-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
