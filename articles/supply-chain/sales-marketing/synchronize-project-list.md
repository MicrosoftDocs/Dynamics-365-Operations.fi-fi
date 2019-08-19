---
title: Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceeen.
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
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843550"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="7b302-103">Finance and Operationsin projektiluetteloiden synkronointi Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="7b302-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b302-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceeen.</span><span class="sxs-lookup"><span data-stu-id="7b302-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7b302-105">[![Liiketoimintaprosessien synkronointi Finance and Operationsin ja Field Servicen välillä](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="7b302-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b302-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="7b302-106">Templates and tasks</span></span>
<span data-ttu-id="7b302-107">Seuraavalla mallilla ja taustalla olevilla tehtävillä synkronoidaan projekteja Microsoft Dynamics 365 for Finance and Operationsista Microsoft Dynamics 365 for Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="7b302-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7b302-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="7b302-108">**Template in Data integration**</span></span>
- <span data-ttu-id="7b302-109">Projektit (Fin and Opsista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="7b302-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="7b302-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="7b302-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="7b302-111">Projektit</span><span class="sxs-lookup"><span data-stu-id="7b302-111">Projects</span></span>

<span data-ttu-id="7b302-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="7b302-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="7b302-113">Tilit (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="7b302-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="7b302-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="7b302-114">Entity set</span></span>
| <span data-ttu-id="7b302-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="7b302-115">Field Service</span></span>           | <span data-ttu-id="7b302-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b302-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="7b302-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="7b302-117">msdynce_externalprojects</span></span> | <span data-ttu-id="7b302-118">Projektit</span><span class="sxs-lookup"><span data-stu-id="7b302-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="7b302-119">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="7b302-119">Entity flow</span></span>
<span data-ttu-id="7b302-120">Projektit luodaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="7b302-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="7b302-121">Projektit, joiden **projektityypiksi** on määritetty **Aika ja materiaali** ja **projektin vaiheeksi** on määritetty **Keskeneräinen**, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="7b302-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="7b302-122">**Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Finance and Operationsin projektien kanssa.</span><span class="sxs-lookup"><span data-stu-id="7b302-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7b302-123">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="7b302-123">Field Service CRM solution</span></span>
<span data-ttu-id="7b302-124">**Ulkoinen projekti** -yksikkö hakee kaikki Finance and Operationsin projektit.</span><span class="sxs-lookup"><span data-stu-id="7b302-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="7b302-125">**Ulkoinen projekti** -kenttä on lisätty **Työtilaus**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="7b302-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="7b302-126">Tämä on valintakenttä, joten työtilauksen merkitseminen projektiin aiheuttaa myyntitilaus yhdistämisen Finance and Operationsin projektiin.</span><span class="sxs-lookup"><span data-stu-id="7b302-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="7b302-127">Kun **järjestelmän tila** **Avoin - käsittelyssä (690 970 000)** muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="7b302-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7b302-128">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="7b302-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="7b302-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b302-129">Finance and Operations</span></span>
<span data-ttu-id="7b302-130">Ota muutosten seuranta käyttöön tietoyksikköprojekteissa.</span><span class="sxs-lookup"><span data-stu-id="7b302-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b302-131">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="7b302-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="7b302-132">Projektit (Fin and Opsista Field Serviceen): Projektit</span><span class="sxs-lookup"><span data-stu-id="7b302-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="7b302-133">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="7b302-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
