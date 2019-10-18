---
title: Projektiluettelon synkronointi Supply Chain Managementista Field Serviceen
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceeen.
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
ms.openlocfilehash: b74a7f0445b3bdad671da4c61e561bc0d9d80cd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251589"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="7bc95-103">Projektiluettelon synkronointi Supply Chain Managementista Field Serviceen</span><span class="sxs-lookup"><span data-stu-id="7bc95-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7bc95-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projekteja synkronoidaan Dynamics 365 Supply Chain Managementista Dynamics 365 Field Serviceeen.</span><span class="sxs-lookup"><span data-stu-id="7bc95-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="7bc95-105">[![Liiketoimintaprosessien synkronointi Supply Chain Managementin ja Field Servicen välillä](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="7bc95-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7bc95-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="7bc95-106">Templates and tasks</span></span>
<span data-ttu-id="7bc95-107">Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa projekteja Supply Chain Managementista Field Serviceen.</span><span class="sxs-lookup"><span data-stu-id="7bc95-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="7bc95-108">**Tietojen integroinnin malli**</span><span class="sxs-lookup"><span data-stu-id="7bc95-108">**Template in Data integration**</span></span>
- <span data-ttu-id="7bc95-109">Projektit (Supply Chain Managementista Field Serviceen)</span><span class="sxs-lookup"><span data-stu-id="7bc95-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="7bc95-110">**Tietojen integrointiprojektin tehtävä**</span><span class="sxs-lookup"><span data-stu-id="7bc95-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="7bc95-111">Projektit</span><span class="sxs-lookup"><span data-stu-id="7bc95-111">Projects</span></span>

<span data-ttu-id="7bc95-112">Seuraavat synkronointitehtävät tarvitaan, ennen kuin projektiluettelo voidaan synkronoida:</span><span class="sxs-lookup"><span data-stu-id="7bc95-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="7bc95-113">Tilit (Salesista Supply Chain Managementiin)</span><span class="sxs-lookup"><span data-stu-id="7bc95-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="7bc95-114">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="7bc95-114">Entity set</span></span>
| <span data-ttu-id="7bc95-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="7bc95-115">Field Service</span></span>           | <span data-ttu-id="7bc95-116">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="7bc95-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="7bc95-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="7bc95-117">msdynce_externalprojects</span></span> | <span data-ttu-id="7bc95-118">Projektit</span><span class="sxs-lookup"><span data-stu-id="7bc95-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="7bc95-119">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="7bc95-119">Entity flow</span></span>
<span data-ttu-id="7bc95-120">Projektit luodaan Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="7bc95-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="7bc95-121">Projektit, joiden **projektityypiksi** on määritetty **Aika ja materiaali** ja **projektin vaiheeksi** on määritetty **Keskeneräinen**, synkronoidaan Field Servicen **Ulkoinen projekti** -yksikköön. Myös projektin numero, nimi ja vaihe sekä asiakastilin tiedot synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="7bc95-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="7bc95-122">**Ulkoinen projekti** -luettelon avulla Field Servicen työtilaukset muodostavat parin Supply Chain Managementin projektien kanssa.</span><span class="sxs-lookup"><span data-stu-id="7bc95-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7bc95-123">Field Service CRM -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="7bc95-123">Field Service CRM solution</span></span>
<span data-ttu-id="7bc95-124">**Ulkoinen projekti** -yksikkö hakee kaikki Supply Chain Managementin projektit.</span><span class="sxs-lookup"><span data-stu-id="7bc95-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="7bc95-125">**Ulkoinen projekti** -kenttä on lisätty **Työtilaus**-yksikköön.</span><span class="sxs-lookup"><span data-stu-id="7bc95-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="7bc95-126">Tämä on valintakenttä, joten työtilauksen merkitseminen projektiin aiheuttaa myyntitilaus yhdistämisen Supply Chain Managementin projektiin.</span><span class="sxs-lookup"><span data-stu-id="7bc95-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="7bc95-127">Kun **järjestelmän tila** **Avoin - käsittelyssä (690 970 000)** muuttuu korkeammaksi tilaksi, **Ulkoinen projekti** -kenttä lukitaan, etkä voi enää lisätä, poistaa tai muuttaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="7bc95-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7bc95-128">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="7bc95-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="7bc95-129">Toimitusketjun hallinta</span><span class="sxs-lookup"><span data-stu-id="7bc95-129">Supply Chain Management</span></span>
<span data-ttu-id="7bc95-130">Ota muutosten seuranta käyttöön tietoyksikköprojekteissa.</span><span class="sxs-lookup"><span data-stu-id="7bc95-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7bc95-131">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="7bc95-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="7bc95-132">Projektit (Supply Chain Managementista Field Serviceen): Projektit</span><span class="sxs-lookup"><span data-stu-id="7bc95-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="7bc95-133">[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="7bc95-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
