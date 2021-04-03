---
title: Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d2364378ce8992666e374ec6f665c180d2fa1981
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258020"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="6239d-103">Työtilausten ja projektin synkronointi Field Servicesta Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="6239d-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6239d-104">Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Dynamics 365 Field Servicestä Dynamics 365 Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="6239d-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6239d-105">[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="6239d-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="6239d-106">Käytetty **Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)** -malli perustuu **Työtilaukset (Field Servicesta Supply Chain Managementiin)** -malliin.</span><span class="sxs-lookup"><span data-stu-id="6239d-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="6239d-107">Lisätietoja on kohdassa [Field Servicen työtilausten synkronointi Supply Chain Managementin myyntitilauksiin](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="6239d-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="6239d-108">Tässä ohjeaiheessa käsitellään kahden mallin eroja:</span><span class="sxs-lookup"><span data-stu-id="6239d-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="6239d-109">**Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)**</span><span class="sxs-lookup"><span data-stu-id="6239d-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="6239d-110">**Työtilaukset (Field Servicesta Supply Chain Managementiin)**</span><span class="sxs-lookup"><span data-stu-id="6239d-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="6239d-111">Pääasiallisin ero on, että tämä malli sisältää työtilaukselle Field Servicessa määritetyn projektinumeron yhdistämismäärityksen, mikä varmistaa, että Supply Chain Managementissa luotu myyntitilaus sisältää projektinumeron ja että laskutus voidaan tehdä liittyvässä projektissa.</span><span class="sxs-lookup"><span data-stu-id="6239d-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="6239d-112">Tämän lisäksi malli käyttää kyselyn ja suodatuksen lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="6239d-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6239d-113">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="6239d-113">Templates and tasks</span></span>

<span data-ttu-id="6239d-114">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="6239d-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="6239d-115">Projektin työtilaukset (Field Servicesta Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="6239d-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="6239d-116">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="6239d-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="6239d-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6239d-117">WorkOrderHeader</span></span>
- <span data-ttu-id="6239d-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6239d-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="6239d-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6239d-119">WorkOrderProduct</span></span>
- <span data-ttu-id="6239d-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6239d-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6239d-121">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6239d-121">Field Service CRM solution</span></span>
<span data-ttu-id="6239d-122">**Ulkoinen projekti** -kenttä on lisätty Työtilaus-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="6239d-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="6239d-123">Tämä kenttä on valintakenttä ja työtilauksen merkitseminen projektiin aiheuttaa myyntitilauksen yhdistämisen Supply Chain Managementin projektiin.</span><span class="sxs-lookup"><span data-stu-id="6239d-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="6239d-124">Kun **Järjestelmän tila** muuttuu Avoin - käsittelyssä (690 970 000) -tilasta korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="6239d-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6239d-125">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="6239d-125">Template mapping in Data integration</span></span>

<span data-ttu-id="6239d-126">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6239d-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="6239d-127">Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="6239d-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="6239d-128">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="6239d-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="6239d-129">Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="6239d-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="6239d-130">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="6239d-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="6239d-131">Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="6239d-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="6239d-132">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="6239d-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="6239d-133">Projektin työtilaukset (Field Servicesta Supply Chain Managementiin): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="6239d-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="6239d-134">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="6239d-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]