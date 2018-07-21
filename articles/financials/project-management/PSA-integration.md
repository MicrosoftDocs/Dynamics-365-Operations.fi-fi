---
title: Project Service Automation
description: "Tämä ratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 Finance ja Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="a4de1-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a4de1-103">Project Service Automation</span></span>

<span data-ttu-id="a4de1-104">Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi tietojen integrointitoiminnolla tietoja Microsoft Dynamics 365 Finance ja Operationsin ja Microsoft Dynamics 365 for Project Service Automationin esiintymien välillä Common Data Servicen kautta.</span><span class="sxs-lookup"><span data-stu-id="a4de1-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="a4de1-105">Tietojen integrointiominaisuuteen sisältyvät integrointimallit mahdollistavat projekteja, projektisopimuksia, projektisopimuksen rivejä, projektisopimuksen rivien välitavoitteita, projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita ja kuluarvioita koskevien tietojen siirtymisen Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="a4de1-106">Jos käytössä on Dynamics 365 for Finance and Operations Enterprise edition 7.3.0, KB 4074835 on asennettava.</span><span class="sxs-lookup"><span data-stu-id="a4de1-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="a4de1-107">Sen avulla voi integroida kiinteähintaisia projekteja.</span><span class="sxs-lookup"><span data-stu-id="a4de1-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="a4de1-108">Jos käytössä on Dynamics 365 for Finance and Operationsin versio 8.0, voit käyttää projektitehtävien integrointia, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja toiminnon lukitsemista.</span><span class="sxs-lookup"><span data-stu-id="a4de1-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="a4de1-109">Jos käytössä on Dynamics 365 for Finance and Operationsin versio 8.0.1, voit synkronoida todelliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="a4de1-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="a4de1-110">Jos käytössä on Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen.</span><span class="sxs-lookup"><span data-stu-id="a4de1-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a4de1-111">Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.</span><span class="sxs-lookup"><span data-stu-id="a4de1-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="a4de1-112">Project Service Automationin integrointiparametrit on määritettävä ennen Project Service Automationin ja Finance and Operationsin integrointia.</span><span class="sxs-lookup"><span data-stu-id="a4de1-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="a4de1-113">Lisätietoja on kohdassa Project Service Automationin integrointiparametrit.</span><span class="sxs-lookup"><span data-stu-id="a4de1-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="a4de1-114">Integrointiratkaisu mahdollistaa suoran synkronoinnin seuraavissa skenaarioissa:</span><span class="sxs-lookup"><span data-stu-id="a4de1-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="a4de1-115">Projektisopimusten ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-116">Projektien luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-117">Projektisopimuksen rivien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-118">Projektisopimuksen rivien välitavoitteiden ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-119">Projektitehtävien ylläpito Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-120">Kulutapahtumaluokkien ylläpito Finance and Operationsissa ja niiden synkronointi suoraan Finance and Operationsista Project Service Automationiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="a4de1-121">Projektin tuntiarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="a4de1-122">Projektin kuluarvioiden luonti Project Service Automationissa ja niiden synkronointi suoraan Project Service Automationista Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="a4de1-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="a4de1-123">Tietojen synkronointi</span><span class="sxs-lookup"><span data-stu-id="a4de1-123">Data synchronization</span></span>
<span data-ttu-id="a4de1-124">Seuraava kuva ilmaisee, miten tiedot synkronoidaan osana Project Service Automationin ja Finance and Operationsin välistä integrointia.</span><span class="sxs-lookup"><span data-stu-id="a4de1-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="a4de1-125">Tällä hetkellä yhtään mallia ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a4de1-125">Not all templates are currently available.</span></span> <span data-ttu-id="a4de1-126">Mallit julkaistaan, kun ne valmistuvat.</span><span class="sxs-lookup"><span data-stu-id="a4de1-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="a4de1-127">[![Project Service Automationin ja Finance and Operationsin integrointi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="a4de1-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="a4de1-128">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="a4de1-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="a4de1-129">Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisua varten on asennettava Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, jossa on vähintään ympäristöpäivitys 12.</span><span class="sxs-lookup"><span data-stu-id="a4de1-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="a4de1-130">Project Service Automationin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="a4de1-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="a4de1-131">Project Service Automationin ja Finance and Operationsin välisen integrointiratkaisun käyttöä varten on asennettava seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="a4de1-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="a4de1-132">Microsoft Dynamics 365 for Project Service Automationin versio 9.0.0.0 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="a4de1-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="a4de1-133">Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (v14) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="a4de1-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="a4de1-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation versio 1.0.0.0 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="a4de1-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="a4de1-135">Asenna Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu Project Service Automationin esiintymään.</span><span class="sxs-lookup"><span data-stu-id="a4de1-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



