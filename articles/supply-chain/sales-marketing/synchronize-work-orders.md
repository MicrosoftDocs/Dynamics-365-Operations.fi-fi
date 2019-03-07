---
title: Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin
description: Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "329847"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="ad92f-103">Projektin sisältävien työtilausten synkronointi Field Servicestä Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="ad92f-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ad92f-104">Ohjeaiheessa käsitellään malleja ja taustalla olevaa tehtävää, joilla projektinumeron sisältävät työtilaukset synkronoidaan Microsoft Dynamics 365 for Field Servicestä Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="ad92f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ad92f-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="ad92f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="ad92f-106">Käytetty **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)** -malli perustuu Prospektista käteiseksi -ratkaisun **Tuotteet (Finance and Operationsista Salesiin) – suora** -malliin.</span><span class="sxs-lookup"><span data-stu-id="ad92f-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="ad92f-107">Lisätietoja on kohdassa [Tuotteet (Finance and Operationsista Salesiin) – suora](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="ad92f-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="ad92f-108">Tässä ohjeaiheessa käsitellään ainoastaan **Field Servicen tuotteet (Finance and Operationsista Field Serviceen)**- ja**Field Servicen tuotteet (Finance and Operationsista Field Serviceen) – suora** -mallien eroja.</span><span class="sxs-lookup"><span data-stu-id="ad92f-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="ad92f-109">Pääasiallisin ero on, että tämä malli sisältää työtilaukselle Field Servicessä määritetyn projektinumeron yhdistämismäärityksen, mikä varmistaa, että Finance and Operationsissa luotu myyntitilaus sisältää projektinumeron ja että laskutus voidaan tehdä liittyvässä projektissa.</span><span class="sxs-lookup"><span data-stu-id="ad92f-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="ad92f-110">Tämän lisäksi malli käyttää kyselyn ja suodatuksen lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="ad92f-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ad92f-111">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="ad92f-111">Templates and tasks</span></span>

<span data-ttu-id="ad92f-112">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="ad92f-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ad92f-113">Projektin työtilaukset (Field Servicestä Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="ad92f-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="ad92f-114">**Tehtävän nimi tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="ad92f-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ad92f-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ad92f-115">WorkOrderHeader</span></span>
- <span data-ttu-id="ad92f-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ad92f-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="ad92f-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ad92f-117">WorkOrderProduct</span></span>
- <span data-ttu-id="ad92f-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ad92f-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ad92f-119">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ad92f-119">Field Service CRM solution</span></span>
<span data-ttu-id="ad92f-120">**Ulkoinen projekti** -kenttä on lisätty Työtilaus-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="ad92f-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="ad92f-121">Kenttä on valinta- ja ostokenttä, joka merkitsee työtilaukseen projektin tunnisteen, jonka jälkeen myyntitilaus yhdistetään Finance and Operationsin projektiin.</span><span class="sxs-lookup"><span data-stu-id="ad92f-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="ad92f-122">Kun **järjestelmän tila** Avoin - käsittelyssä (690,970,000) muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="ad92f-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ad92f-123">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ad92f-123">Template mapping in Data integration</span></span>

<span data-ttu-id="ad92f-124">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ad92f-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="ad92f-125">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ad92f-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="ad92f-126">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="ad92f-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="ad92f-127">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ad92f-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="ad92f-128">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="ad92f-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="ad92f-129">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ad92f-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="ad92f-130">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="ad92f-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="ad92f-131">Projektin työtilaukset (Field Servicestä Finance and Operationsiin): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ad92f-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="ad92f-132">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="ad92f-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
