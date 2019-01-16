---
title: Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen
description: "Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla fyysiset varastot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="55946-103">Finance and Operationsin fyysisten varastojen synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="55946-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="55946-104">Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla fyysiset varastot synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="55946-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="55946-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="55946-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="55946-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="55946-106">Templates and tasks</span></span>
<span data-ttu-id="55946-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin fyysiset varastot Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="55946-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="55946-108">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="55946-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="55946-109">Varastot (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="55946-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="55946-110">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="55946-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="55946-111">Varasto</span><span class="sxs-lookup"><span data-stu-id="55946-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="55946-112">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="55946-112">Entity set</span></span>
| <span data-ttu-id="55946-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="55946-113">Field Service</span></span>    | <span data-ttu-id="55946-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="55946-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="55946-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="55946-115">msdyn_warehouses</span></span> | <span data-ttu-id="55946-116">Varastot</span><span class="sxs-lookup"><span data-stu-id="55946-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="55946-117">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="55946-117">Entity flow</span></span>
<span data-ttu-id="55946-118">Finance and Operationsissa luodut ja ylläpidetyt fyysiset varastot voidaan synkronoida Field Serviceen Common Data Servicen (CDS) tietojen integrointiprojektilla.</span><span class="sxs-lookup"><span data-stu-id="55946-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="55946-119">Field Serviceen synkronoitavia varastoja voidaan ohjata projektin kyselyn ja suodatuksen lisäasetuksilla.</span><span class="sxs-lookup"><span data-stu-id="55946-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="55946-120">Finance and Operationsista synkronoitavat fyysiset varastot luodaan Field Servicessä siten, että Ylläpidetään ulkoisesti -kentän asetukseksi määritetään Kyllä. Lisäksi tietue on vain luku -muotoinen.</span><span class="sxs-lookup"><span data-stu-id="55946-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="55946-121">Field Service CRM -ratkaisu Field Servicen ja Finance and Operationsin integraation tukemiseen tarvitaan Field Service CRM -ratkaisun lisätoiminto.</span><span class="sxs-lookup"><span data-stu-id="55946-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="55946-122">Ratkaisu sisältää seuraavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="55946-122">The solution includes the following changes.</span></span>
<span data-ttu-id="55946-123">**Ylläpidetään ulkoisesti** -kenttä on lisätty **Varasto (msdyn_warehouses)** -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="55946-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="55946-124">Tämä kenttä auttaa määrittämään, käsitelläänkö varastoa Operationsista vai onko se vain Field Servicessä.</span><span class="sxs-lookup"><span data-stu-id="55946-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="55946-125">Kyllä – varasto on peräisin Finance and Operationsista eikä sitä voi muokata Salesissa.</span><span class="sxs-lookup"><span data-stu-id="55946-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="55946-126">Ei – varasto annettiin suoraan Field Servicessä, jossa sitä myös ylläpidetään.</span><span class="sxs-lookup"><span data-stu-id="55946-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="55946-127">**Ylläpidetään ulkoisesti** -kenttää auttaa hallitsemaan varaston tasojen, oikaisujen, siirtojen ja käytön synkronointia työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="55946-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="55946-128">Vain varastoja, joiden **Ylläpidetään ulkoisesti** = Kyllä, voidaan käyttää suoraan synkronointiin toisessa järjestelmässä olevaan samaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="55946-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="55946-129">Huomautus: Field Servicessä voi luoda useita varastoja (kun **Ylläpidetään ulkoisesti** = Ei) ja ne voi sitten yhdistää yhteen varastoon Finance and Operationsissa kyselyn ja suodatuksen lisäasetustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="55946-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="55946-130">Tämä menettelyä käytetään tilanteissa, joissa Field Servicellä halutaan hallita tarkkaa varastotasoa ja joissa vain päivitykset lähetetään Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="55946-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="55946-131">Tässä tapauksessa Field Service ei saa varastotasopäivityksiä Finance and Operationsista.</span><span class="sxs-lookup"><span data-stu-id="55946-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="55946-132">Lisätietoja on kohdissa Field Servicen varasto-oikaisujen synkronointi Finance and Operationsiin ja Field Servicen työtilausten synkronointi projekteihin Finance and Operationsissa linkitettyihin myyntitilauksiin.</span><span class="sxs-lookup"><span data-stu-id="55946-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="55946-133">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="55946-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="55946-134">Tietojen integrointiprojektissa</span><span class="sxs-lookup"><span data-stu-id="55946-134">In the Data Integration project</span></span>
<span data-ttu-id="55946-135">Ennen varastojen synkronointia projektin kyselyn ja suodatuksen lisäasetukset on päivitettävä sisältämään vain varastot, jotka haluat tuoda Finance and Operationsista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="55946-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="55946-136">Huomaa, että Field Servicen varasto tarvitaan, jotta sitä voidaan käyttää työtilauksissa, oikaisuissa ja siirroissa.</span><span class="sxs-lookup"><span data-stu-id="55946-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="55946-137">**msdyn_warehouses**-kohteen **integrointiavaimen** varmistaminen</span><span class="sxs-lookup"><span data-stu-id="55946-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="55946-138">Siirry tietojen integrointiin</span><span class="sxs-lookup"><span data-stu-id="55946-138">Go to Data Integration</span></span>
2. <span data-ttu-id="55946-139">Valitse **Yhteysjoukko**-välilehti</span><span class="sxs-lookup"><span data-stu-id="55946-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="55946-140">Valitse yhteysjoukko, jota käytetään työtilauksen synkronointiin</span><span class="sxs-lookup"><span data-stu-id="55946-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="55946-141">Valitse **Integrointiavain**-välilehti</span><span class="sxs-lookup"><span data-stu-id="55946-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="55946-142">Etsi msdyn_warehouses ja tarkista, että avain **msdyn_name (nimi)** on lisätty.</span><span class="sxs-lookup"><span data-stu-id="55946-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="55946-143">Jos avainta ei näy, lisää se napsauttamalla **Lisää avain** ja **Tallenna** sivun yläosassa</span><span class="sxs-lookup"><span data-stu-id="55946-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="55946-144">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="55946-144">Template mapping in Data integration</span></span>

<span data-ttu-id="55946-145">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="55946-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="55946-146">Varastot (Finance and Operationsista Field Serviceen): varasto</span><span class="sxs-lookup"><span data-stu-id="55946-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="55946-147">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="55946-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

