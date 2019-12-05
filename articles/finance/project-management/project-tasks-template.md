---
title: Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
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
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770263"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3bf89-103">Projektitehtävien synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin</span><span class="sxs-lookup"><span data-stu-id="3bf89-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3bf89-104">Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektitehtäviä synkronoidaan suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeiin.</span><span class="sxs-lookup"><span data-stu-id="3bf89-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3bf89-105">Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytettävissä versiossa 8.0.</span><span class="sxs-lookup"><span data-stu-id="3bf89-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="3bf89-106">Jos käytät Enterprise edition -versiota 7.3.0 sen jälkeen, kun KB 4132657 ja KB 4132660 on asennettu, voit käyttää malleja integroidaksesi projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittääksesi toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="3bf89-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="3bf89-107">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="3bf89-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="3bf89-108">Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.</span><span class="sxs-lookup"><span data-stu-id="3bf89-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3bf89-109">Tiedonkulku Project Service Automationista Financeen</span><span class="sxs-lookup"><span data-stu-id="3bf89-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="3bf89-110">Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="3bf89-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3bf89-111">Tietojen integrointiominaisuudessa käytettävissä oleva integrointimalli mahdollistaa projektitehtäviä koskevan tiedonkulun Project Service Automationista Financeen.</span><span class="sxs-lookup"><span data-stu-id="3bf89-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3bf89-112">Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.</span><span class="sxs-lookup"><span data-stu-id="3bf89-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3bf89-113">[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3bf89-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="3bf89-114">Malli ja tehtävä</span><span class="sxs-lookup"><span data-stu-id="3bf89-114">Template and task</span></span>

<span data-ttu-id="3bf89-115">Saat mallin käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.</span><span class="sxs-lookup"><span data-stu-id="3bf89-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3bf89-116">Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektitehtävät Project Service Automationista Financeen:</span><span class="sxs-lookup"><span data-stu-id="3bf89-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3bf89-117">**Mallin nimi tietojen integroinnissa:** projektin tehtävät (PSA:sta Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="3bf89-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3bf89-118">**Tehtävän nimi projektissa:** Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3bf89-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="3bf89-119">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="3bf89-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="3bf89-120">Yksikköjoukko</span><span class="sxs-lookup"><span data-stu-id="3bf89-120">Entity set</span></span>

| <span data-ttu-id="3bf89-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3bf89-121">Project Service Automation</span></span> | <span data-ttu-id="3bf89-122">Myyntitiedot</span><span class="sxs-lookup"><span data-stu-id="3bf89-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="3bf89-123">Projektitehtävät</span><span class="sxs-lookup"><span data-stu-id="3bf89-123">Project Tasks</span></span>              | <span data-ttu-id="3bf89-124">Projektitehtävän integrointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="3bf89-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3bf89-125">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="3bf89-125">Entity flow</span></span>

<span data-ttu-id="3bf89-126">Projektitehtäviä hallitaan Project Service Automationissa ja ne synkronoidaan Financeen projektitoimintoina.</span><span class="sxs-lookup"><span data-stu-id="3bf89-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3bf89-127">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="3bf89-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="3bf89-128">Projektisopimukset ja projektit on synkronoitava, ennen kuin projektitehtävät voidaan synkronoida.</span><span class="sxs-lookup"><span data-stu-id="3bf89-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="3bf89-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3bf89-129">Power Query</span></span>

<span data-ttu-id="3bf89-130">Jos seuraavat ehdot toteutuvat, tietojen suodattamiseen on käytettävä Microsoft Power Query for Exceliä:</span><span class="sxs-lookup"><span data-stu-id="3bf89-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="3bf89-131">Projektitehtävässä on resurssikohtaisia tietueita.</span><span class="sxs-lookup"><span data-stu-id="3bf89-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="3bf89-132">Jos Power Queryä on käytettävä, noudata seuraavaa ohjeistusta:</span><span class="sxs-lookup"><span data-stu-id="3bf89-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="3bf89-133">Projektitehtävät (PSA:sta Fin and Opsiiin) -mallissa on oletussuodatin, joka jättää projektitehtävän resurssikohtaiset tietueet pois, kun **IsLineTask**-suodatinasetukseksi on määritetty **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="3bf89-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="3bf89-134">Jos luot oman mallin, tämä suodatin on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="3bf89-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3bf89-135">Mallin yhdistäminen tietojen integroinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="3bf89-135">Template mapping in Data integration</span></span>

<span data-ttu-id="3bf89-136">Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="3bf89-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="3bf89-137">Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.</span><span class="sxs-lookup"><span data-stu-id="3bf89-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3bf89-138">[![Mallin yhdistäminen](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="3bf89-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
