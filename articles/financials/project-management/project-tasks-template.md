---
title: Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7ea5036682ad5b61fe56acd20a591cccc01f2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838316"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3d75c-103">Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin</span><span class="sxs-lookup"><span data-stu-id="3d75c-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d75c-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="3d75c-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="3d75c-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="3d75c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="3d75c-106">Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="3d75c-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="3d75c-107">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="3d75c-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="3d75c-108">Todellisten tietojen integrointi on mahdollista Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.1 tai sitä uudemmassa versiossa.</span><span class="sxs-lookup"><span data-stu-id="3d75c-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3d75c-109">Tiedonkulku Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="3d75c-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="3d75c-110">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="3d75c-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="3d75c-111">Tietojen integrointiominaisuudessa käytettävissä oleva integrointimalli mahdollistaa projektitehtäviä koskevan tiedonkulun Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="3d75c-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="3d75c-112">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="3d75c-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="3d75c-113">[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3d75c-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="3d75c-114">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="3d75c-114">Template and task</span></span>

<span data-ttu-id="3d75c-115">Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="3d75c-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3d75c-116">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektitehtävät Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="3d75c-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="3d75c-117">**Mallin nimi tietojen integroinnissa:** projektin tehtävät (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="3d75c-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3d75c-118">**Tehtävän nimi projektissa:** Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3d75c-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="3d75c-119">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="3d75c-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="3d75c-120">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="3d75c-120">Entity set</span></span>

| <span data-ttu-id="3d75c-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3d75c-121">Project Service Automation</span></span> | <span data-ttu-id="3d75c-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3d75c-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="3d75c-123">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3d75c-123">Project Tasks</span></span>              | <span data-ttu-id="3d75c-124">Projektitehtävän integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="3d75c-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3d75c-125">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="3d75c-125">Entity flow</span></span>

<span data-ttu-id="3d75c-126">Projektitehtäviä hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektitoimintoina.</span><span class="sxs-lookup"><span data-stu-id="3d75c-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3d75c-127">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="3d75c-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="3d75c-128">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="3d75c-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="3d75c-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3d75c-129">Power Query</span></span>

<span data-ttu-id="3d75c-130">Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Query for Exceliä:</span><span class="sxs-lookup"><span data-stu-id="3d75c-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="3d75c-131">Projektitehtävässä on resurssikohtaisia tietueita.</span><span class="sxs-lookup"><span data-stu-id="3d75c-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="3d75c-132">Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:</span><span class="sxs-lookup"><span data-stu-id="3d75c-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="3d75c-133">Projektitehtävät (PSA:sta Fin and Opsiiin) -mallissa on oletussuodatin, joka jättää projektitehtävän resurssikohtaiset tietueet pois, kun **IsLineTask**-suodatinasetukseksi on määritetty **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="3d75c-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="3d75c-134">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="3d75c-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3d75c-135">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="3d75c-135">Template mapping in Data integration</span></span>

<span data-ttu-id="3d75c-136">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="3d75c-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="3d75c-137">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="3d75c-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="3d75c-138">[![Mallin yhdistäminen](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="3d75c-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
