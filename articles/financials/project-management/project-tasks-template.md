---
title: "Projektitehtävien synkronointi Project Service Automationista"
description: "Tässä ohjeaiheessa käsitellään mallia ja taustalla olevaa tehtävää, joilla projektitehtävät tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="06662-103">Projektitehtävien synkronointi Project Service Automationista suoraan Finance and Operationsin projektitoimintoihin</span><span class="sxs-lookup"><span data-stu-id="06662-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="06662-104">Tässä ohjeaiheessa käsitellään mallia ja taustalla olevaa tehtävää, joilla projektitehtävät tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="06662-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="06662-105">Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="06662-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="06662-106">Tiedonkulku Project Service Automationista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="06662-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="06662-107">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="06662-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="06662-108">Tietojen integrointiominaisuudessa käytettävissä oleva integrointimalli mahdollistaa projektitehtäviä koskevan tiedonkulun Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="06662-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="06662-109">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.</span><span class="sxs-lookup"><span data-stu-id="06662-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="06662-110">[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="06662-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="06662-111">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="06662-111">Template and task</span></span>

<span data-ttu-id="06662-112">Saat mallin käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="06662-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="06662-113">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektitehtävät Project Service Automationista Finance and Operationsiin:</span><span class="sxs-lookup"><span data-stu-id="06662-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="06662-114">-**Mallin nimi tietojen integroinnissa:** Projektitehtävät (PSA:sta Fin and Opsiin) -**Projektin tehtävän nimi:** Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="06662-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="06662-115">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="06662-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="06662-116">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="06662-116">Entity set</span></span>

|<span data-ttu-id="06662-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="06662-117">Project Service Automation</span></span>               | <span data-ttu-id="06662-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06662-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="06662-119">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="06662-119">Project Tasks</span></span>                           | <span data-ttu-id="06662-120">Projektitehtävän integrointiyksikkö.</span><span class="sxs-lookup"><span data-stu-id="06662-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="06662-121">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="06662-121">Entity flow</span></span>

<span data-ttu-id="06662-122">Projektitehtäviä hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektitoimintoina.</span><span class="sxs-lookup"><span data-stu-id="06662-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="06662-123">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="06662-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="06662-124">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="06662-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="06662-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="06662-125">Power Query</span></span>

<span data-ttu-id="06662-126">Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Queryä:</span><span class="sxs-lookup"><span data-stu-id="06662-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="06662-127">Projektitehtävässä on resurssikohtaisia tietueita.</span><span class="sxs-lookup"><span data-stu-id="06662-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="06662-128">Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:</span><span class="sxs-lookup"><span data-stu-id="06662-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="06662-129">Projektitehtävät (PSA:sta Fin and Opsiiin) -mallissa on oletussuodatin, joka jättää projektitehtävän resurssikohtaiset tietueet pois, kun **IsLineTask**-suodatinasetukseksi on määritetty **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="06662-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="06662-130">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="06662-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="06662-131">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="06662-131">Template mapping in Data integration</span></span>

<span data-ttu-id="06662-132">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="06662-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="06662-133">Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.</span><span class="sxs-lookup"><span data-stu-id="06662-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="06662-134">[![Mallin yhdistäminen](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="06662-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


