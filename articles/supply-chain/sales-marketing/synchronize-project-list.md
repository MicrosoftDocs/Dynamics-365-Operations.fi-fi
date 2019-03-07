---
title: Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceeen.
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
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "312505"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="13bcb-103">Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="13bcb-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13bcb-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceeen.</span><span class="sxs-lookup"><span data-stu-id="13bcb-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="13bcb-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="13bcb-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="13bcb-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="13bcb-106">Templates and tasks</span></span>
<span data-ttu-id="13bcb-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan projekteja Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="13bcb-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="13bcb-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="13bcb-108">**Template in Data integration**</span></span>
- <span data-ttu-id="13bcb-109">Projektit (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="13bcb-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="13bcb-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="13bcb-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="13bcb-111">Projektit</span><span class="sxs-lookup"><span data-stu-id="13bcb-111">Projects</span></span>

<span data-ttu-id="13bcb-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="13bcb-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="13bcb-113">Tilit (Salesista Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="13bcb-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="13bcb-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="13bcb-114">Entity set</span></span>
| <span data-ttu-id="13bcb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="13bcb-115">Field Service</span></span>           | <span data-ttu-id="13bcb-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="13bcb-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="13bcb-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="13bcb-117">msdynce_externalprojects</span></span> | <span data-ttu-id="13bcb-118">Projektit</span><span class="sxs-lookup"><span data-stu-id="13bcb-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="13bcb-119">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="13bcb-119">Entity flow</span></span>
<span data-ttu-id="13bcb-120">Projektit luodaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="13bcb-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="13bcb-121">Projektit, joiden **projektityypiksi** on määritetty **Aika ja materiaali** ja **projektin vaiheeksi** on määritetty **Keskeneräinen**, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="13bcb-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="13bcb-122">**Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Finance and Operationsin projektien kanssa.</span><span class="sxs-lookup"><span data-stu-id="13bcb-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="13bcb-123">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="13bcb-123">Field Service CRM solution</span></span>
<span data-ttu-id="13bcb-124">**Ulkoinen projekti** -yksikkö hakee kaikki Finance and Operationsin projektit.</span><span class="sxs-lookup"><span data-stu-id="13bcb-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="13bcb-125">**Ulkoinen projekti** -kenttä on lisätty **Työtilaus**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="13bcb-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="13bcb-126">Tämä on valintakenttä, joten työtilauksen merkitseminen projektiin aiheuttaa myyntitilaus yhdistämisen Finance and Operationsin projektiin.</span><span class="sxs-lookup"><span data-stu-id="13bcb-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="13bcb-127">Kun **järjestelmän tila** **Avoin - käsittelyssä (690 970 000)** muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="13bcb-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="13bcb-128">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="13bcb-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="13bcb-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="13bcb-129">Finance and Operations</span></span>
<span data-ttu-id="13bcb-130">Ota muutosten seuranta käyttöön tietoyksikköprojekteissa.</span><span class="sxs-lookup"><span data-stu-id="13bcb-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="13bcb-131">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="13bcb-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="13bcb-132">Projektit (Finance and Operationsista Field Serviceen): projektit</span><span class="sxs-lookup"><span data-stu-id="13bcb-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="13bcb-133">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="13bcb-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
