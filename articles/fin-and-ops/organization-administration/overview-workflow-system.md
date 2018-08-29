---
title: "Työnkulkujärjestelmä"
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmää."
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 770796b42e79ad616b469e1dbf5149789bff0788
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="workflow-system"></a><span data-ttu-id="14918-103">Työnkulkujärjestelmä</span><span class="sxs-lookup"><span data-stu-id="14918-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14918-104">Tässä aiheessa käsitellään Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="14918-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="14918-105">Mikä on työnkulku?</span><span class="sxs-lookup"><span data-stu-id="14918-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="14918-106">Termi *työnkulku* voidaan määrittää kahdella tavalla: järjestelmänä tai liiketoimintaprosessina.</span><span class="sxs-lookup"><span data-stu-id="14918-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="14918-107">Työnkulku järjestelmänä</span><span class="sxs-lookup"><span data-stu-id="14918-107">Workflow is a system</span></span>

<span data-ttu-id="14918-108">Työnkulku on järjestelmä, joka asennetaan Finance and Operationsin mukana ja jota suoritetaan Application Object Server (AOS) -palvelimessa.</span><span class="sxs-lookup"><span data-stu-id="14918-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="14918-109">Työnkulkujärjestelmän toimintojen avulla voit luoda yksittäisiä työnkulkuja eli liiketoimintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="14918-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="14918-110">Työnkulku liiketoimintaprosessina</span><span class="sxs-lookup"><span data-stu-id="14918-110">Workflow is a business process</span></span>

<span data-ttu-id="14918-111">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="14918-111">A workflow represents a business process.</span></span> <span data-ttu-id="14918-112">Se määrittää, kuinka asiakirja kulkee tai siirtyy järjestelmässä kuvaamalla kenen on suoritettava tehtävä loppuun, tehtävä päätös tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="14918-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="14918-113">Seuraavassa kuvassa on esimerkkityönkulku kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="14918-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![Työnkulku, jonka elementtejä on delegoitu käyttäjille](./media/workflow_user.gif) 

<span data-ttu-id="14918-115">Tässä työnkulkuesimerkissä Sam lähettää kuluraportin, jonka summa on 7 000 USD.</span><span class="sxs-lookup"><span data-stu-id="14918-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="14918-116">Ivanin on tarkistettava Samin hänelle lähettämät kuitit.</span><span class="sxs-lookup"><span data-stu-id="14918-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="14918-117">Sen jälkeen Frankin ja Suen on hyväksyttävä kuluraportti.</span><span class="sxs-lookup"><span data-stu-id="14918-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="14918-118">Oletetaan, että Sam lähettää kuluraportin, jonka summa on 11 000 Yhdysvaltain dollaria (USD).</span><span class="sxs-lookup"><span data-stu-id="14918-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="14918-119">Tässä tapauksessa Ivanin on tarkistettava kuitit ja Frankin, Suen ja Annin hyväksyttävä kuluraportti.</span><span class="sxs-lookup"><span data-stu-id="14918-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="14918-120"> Työnkulkujärjestelmän edut</span><span class="sxs-lookup"><span data-stu-id="14918-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="14918-121">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="14918-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="14918-122">**Yhdenmukaiset prosessit** — Voit määrittää, miten tietyt asiakirjat, kuten ostoehdotukset ja kuluraportit käsitellään.</span><span class="sxs-lookup"><span data-stu-id="14918-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="14918-123">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="14918-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="14918-124">**Prosessin näkyvyys** – Voit seurata työnkulun esiintymien tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="14918-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="14918-125">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="14918-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="14918-126">**Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät.</span><span class="sxs-lookup"><span data-stu-id="14918-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="14918-127">Työnkulun sisältö</span><span class="sxs-lookup"><span data-stu-id="14918-127">Workflow content</span></span>

+ [<span data-ttu-id="14918-128">Työnkulun arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="14918-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="14918-129">Työnkulun elementit</span><span class="sxs-lookup"><span data-stu-id="14918-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="14918-130">Työnkulkutehtävät</span><span class="sxs-lookup"><span data-stu-id="14918-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="14918-131">Työnkulun luominen</span><span class="sxs-lookup"><span data-stu-id="14918-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="14918-132">Työnkulkuominaisuuksien asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="14918-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="14918-133">Manuaalisen tehtävän konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="14918-134">Automaattisen tehtävän määrittäminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="14918-135">Hyväksyntäprosessin lisääminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="14918-136">Hyväksyntävaiheen lisääminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="14918-137">Manuaalisen päätöksen konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="14918-138">Ehdollisen päätöksen konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="14918-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="14918-139">Rinnakkaisen tehtävän määrittäminen työnkulussa</span><span class="sxs-lookup"><span data-stu-id="14918-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="14918-140">Määritä rinnakkainen haara työnkulussa</span><span class="sxs-lookup"><span data-stu-id="14918-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="14918-141">Rivinimikkeen työnkulun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="14918-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

