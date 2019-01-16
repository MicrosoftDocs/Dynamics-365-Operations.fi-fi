---
title: Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen
description: "Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektit synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: fi-fi
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="980a6-103">Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="980a6-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="980a6-104">Ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla projektit synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="980a6-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="980a6-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="980a6-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="980a6-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="980a6-106">Templates and tasks</span></span>
<span data-ttu-id="980a6-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan Microsoft Dynamics 365 for Finance and Operationsin projektit Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="980a6-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="980a6-108">**Mallin nimi Tietojen integroinnissa:**</span><span class="sxs-lookup"><span data-stu-id="980a6-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="980a6-109">Projektit (Finance and Operationsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="980a6-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="980a6-110">**Tehtävien nimet tietojen integrointiprojektissa:**</span><span class="sxs-lookup"><span data-stu-id="980a6-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="980a6-111">Projektit</span><span class="sxs-lookup"><span data-stu-id="980a6-111">Projects</span></span>

<span data-ttu-id="980a6-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="980a6-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="980a6-113">Tilit (Salesista Finance and Operationsiin)</span><span class="sxs-lookup"><span data-stu-id="980a6-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="980a6-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="980a6-114">Entity set</span></span>
<span data-ttu-id="980a6-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="980a6-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="980a6-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="980a6-116">Field Service</span></span>           | <span data-ttu-id="980a6-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="980a6-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="980a6-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="980a6-118">msdynce_externalprojects</span></span> | <span data-ttu-id="980a6-119">Projektit</span><span class="sxs-lookup"><span data-stu-id="980a6-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="980a6-120">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="980a6-120">Entity flow</span></span>
<span data-ttu-id="980a6-121">Projektit luodaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="980a6-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="980a6-122">Projektit, joiden **projektityyppi** on aika ja joiden materiaali ja **projektin vaihe** on keskeneräinen, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="980a6-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="980a6-123">**Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Finance and Operationsin projektien kanssa.</span><span class="sxs-lookup"><span data-stu-id="980a6-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="980a6-124">Field Service CRM -ratkaisun Ulkoinen projekti on uusi yksikkö, johon kaikki Operationsin projektit kerätään.</span><span class="sxs-lookup"><span data-stu-id="980a6-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="980a6-125">Ulkoinen projekti -kenttä on lisätty Työtilaus-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="980a6-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="980a6-126">Kenttä on valinta- ja ostokenttä, joka merkitsee työtilaukseen projektin tunnisteen, jonka jälkeen myyntitilaus yhdistetään Operationsin projektiin.</span><span class="sxs-lookup"><span data-stu-id="980a6-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="980a6-127">Kun järjestelmän tila Avoin - käsittelyssä (690,970,000) muuttuu korkeammaksi tilaksi, Ulkoinen projekti -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="980a6-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="980a6-128">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="980a6-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="980a6-129">Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="980a6-129">In Finance and Operations</span></span>
<span data-ttu-id="980a6-130">Muutosten seurannan ottaminen käyttöön tietoyksikköprojekteissa</span><span class="sxs-lookup"><span data-stu-id="980a6-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="980a6-131">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="980a6-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="980a6-132">Projektit (Finance and Operationsista Field Serviceen): projektit</span><span class="sxs-lookup"><span data-stu-id="980a6-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="980a6-133">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="980a6-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

