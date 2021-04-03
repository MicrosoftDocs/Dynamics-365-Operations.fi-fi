---
title: Työnkulkujärjestelmän yleiskatsaus
description: Tässä ohjeaiheessa käsitellään työnkulkujärjestelmää.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd8fba1376dc5e3dbfea888ca5ff5fdeb608fc9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560698"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="f3ce0-103">Työnkulkujärjestelmän yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f3ce0-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3ce0-104">Tässä ohjeaiheessa käsitellään työnkulkujärjestelmää.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="f3ce0-105">Mikä on työnkulku?</span><span class="sxs-lookup"><span data-stu-id="f3ce0-105">What is workflow?</span></span>

<span data-ttu-id="f3ce0-106">Termi *työnkulku* voidaan määrittää kahdella tavalla: järjestelmänä tai liiketoimintaprosessina.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="f3ce0-107">Työnkulku järjestelmänä</span><span class="sxs-lookup"><span data-stu-id="f3ce0-107">Workflow is a system</span></span>

<span data-ttu-id="f3ce0-108">Työnkulku on järjestelmä, joka suoritetaan Application Object Server (AOS) -palvelimessa.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="f3ce0-109">Työnkulkujärjestelmän toimintojen avulla voit luoda yksittäisiä työnkulkuja eli liiketoimintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="f3ce0-110">Työnkulku liiketoimintaprosessina</span><span class="sxs-lookup"><span data-stu-id="f3ce0-110">Workflow is a business process</span></span>

<span data-ttu-id="f3ce0-111">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-111">A workflow represents a business process.</span></span> <span data-ttu-id="f3ce0-112">Se määrittää, kuinka asiakirja kulkee tai siirtyy järjestelmässä kuvaamalla kenen on suoritettava tehtävä loppuun, tehtävä päätös tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="f3ce0-113">Seuraavassa kuvassa on esimerkkityönkulku kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Työnkulku, jonka elementtejä on delegoitu käyttäjille](./media/workflow_user.gif)

<span data-ttu-id="f3ce0-115">Tässä työnkulkuesimerkissä Sam lähettää kuluraportin, jonka summa on 7 000 USD.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="f3ce0-116">Ivanin on tarkistettava Samin hänelle lähettämät kuitit.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="f3ce0-117">Sen jälkeen Frankin ja Suen on hyväksyttävä kuluraportti.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="f3ce0-118">Oletetaan, että Sam lähettää kuluraportin, jonka summa on 11 000 Yhdysvaltain dollaria (USD).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="f3ce0-119">Tässä tapauksessa Ivanin on tarkistettava kuitit ja Frankin, Suen ja Annin hyväksyttävä kuluraportti.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="f3ce0-120"> Työnkulkujärjestelmän edut</span><span class="sxs-lookup"><span data-stu-id="f3ce0-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="f3ce0-121">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="f3ce0-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="f3ce0-122">**Yhdenmukaiset prosessit** — Voit määrittää, miten tietyt asiakirjat, kuten ostoehdotukset ja kuluraportit käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="f3ce0-123">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="f3ce0-124">**Prosessin näkyvyys** – Voit seurata työnkulun esiintymien tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="f3ce0-125">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="f3ce0-126">**Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="f3ce0-127">Työnkulun sisältö</span><span class="sxs-lookup"><span data-stu-id="f3ce0-127">Workflow content</span></span>

+ [<span data-ttu-id="f3ce0-128">Työnkulkujärjestelmän arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="f3ce0-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="f3ce0-129">Työnkulun elementit</span><span class="sxs-lookup"><span data-stu-id="f3ce0-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="f3ce0-130">Toiminnot hyväksyntäprosessien työnkulussa</span><span class="sxs-lookup"><span data-stu-id="f3ce0-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="f3ce0-131">Työnkulkujen luonnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f3ce0-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="f3ce0-132">Työnkulkuominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3ce0-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="f3ce0-133">Manuaalisten tehtävien konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="f3ce0-134">Automaattisten tehtävien määrittäminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="f3ce0-135">Hyväksyntäprosessien lisääminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="f3ce0-136">Hyväksyntävaiheiden lisääminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="f3ce0-137">Manuaalisten päätösten konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="f3ce0-138">Ehdollisten päätösten konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f3ce0-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="f3ce0-139">Rinnakkaisten tehtävien määrittäminen työnkulussa</span><span class="sxs-lookup"><span data-stu-id="f3ce0-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="f3ce0-140">Määritä rinnakkaiset haarat työnkulussa</span><span class="sxs-lookup"><span data-stu-id="f3ce0-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="f3ce0-141">Rivinimikkeen työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f3ce0-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="f3ce0-142">Työnkulun usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="f3ce0-142">Workflow FAQ</span></span>](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]