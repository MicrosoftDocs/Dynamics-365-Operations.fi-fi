---
title: Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536730"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="b72b3-103">Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="b72b3-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b72b3-104">Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="b72b3-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b72b3-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b72b3-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="b72b3-106">Käytetty **Projektin työtilaukset (Field Servicestä Finance and Operationsiin)** -malli perustuu **Työtilaukset (Field Servicestä Finance and Operationsiin)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="b72b3-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="b72b3-107">Lisätietoja on kohdassa [Field Servicen työtilausten synkronointi Finance and Operationsin myyntitilauksiin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="b72b3-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="b72b3-108">Tässä ohjeaiheessa käsitellään kahden mallin eroja:</span><span class="sxs-lookup"><span data-stu-id="b72b3-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="b72b3-109">**Projektin työtilaukset (Field Servicestä Finance and Operationsiin)**</span><span class="sxs-lookup"><span data-stu-id="b72b3-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="b72b3-110">**Työtilaukset (Field Servicestä Finance and Operationsiin)**</span><span class="sxs-lookup"><span data-stu-id="b72b3-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="b72b3-111">Pääasiallisin ero on, että tämä malli sisältää työtilaukselle Field Servicessä määritetyn projektinumeron yhdistämismäärityksen, mikä varmistaa, että Finance and Operationsissa luotu myyntitilaus sisältää projektinumeron ja että laskutus voidaan tehdä liittyvässä projektissa.</span><span class="sxs-lookup"><span data-stu-id="b72b3-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="b72b3-112">Tämän lisäksi malli käyttää kyselyn ja suodatuksen lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="b72b3-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b72b3-113">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="b72b3-113">Templates and tasks</span></span>

<span data-ttu-id="b72b3-114">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="b72b3-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="b72b3-115">Projektin työtilaukset (Field Servicestä Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="b72b3-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="b72b3-116">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="b72b3-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="b72b3-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b72b3-117">WorkOrderHeader</span></span>
- <span data-ttu-id="b72b3-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b72b3-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="b72b3-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b72b3-119">WorkOrderProduct</span></span>
- <span data-ttu-id="b72b3-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b72b3-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b72b3-121">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="b72b3-121">Field Service CRM solution</span></span>
<span data-ttu-id="b72b3-122">**Ulkoinen projekti** -kenttä on lisätty Työtilaus-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="b72b3-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="b72b3-123">Kenttä on valinta- ja ostokenttä, joka merkitsee työtilaukseen projektin tunnisteen, jonka jälkeen myyntitilaus yhdistetään Finance and Operationsin projektiin.</span><span class="sxs-lookup"><span data-stu-id="b72b3-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="b72b3-124">Kun **järjestelmän tila** Avoin - käsittelyssä (690,970,000) muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="b72b3-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b72b3-125">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="b72b3-125">Template mapping in Data integration</span></span>

<span data-ttu-id="b72b3-126">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b72b3-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="b72b3-127">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="b72b3-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="b72b3-128">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="b72b3-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="b72b3-129">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="b72b3-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="b72b3-130">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="b72b3-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="b72b3-131">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="b72b3-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="b72b3-132">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="b72b3-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="b72b3-133">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="b72b3-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="b72b3-134">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="b72b3-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
