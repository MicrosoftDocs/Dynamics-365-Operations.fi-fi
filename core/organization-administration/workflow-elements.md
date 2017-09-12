---
title: "Työnkulun elementit"
description: "Tässä artikkelissa kuvataan eri osia, jotka muodostavat työnkulun."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5620a91ff9f300bed782170307a295ab79fc5b2e
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="003b4-103">Työnkulun elementit</span><span class="sxs-lookup"><span data-stu-id="003b4-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="003b4-104">Tässä artikkelissa kuvataan eri osia, jotka muodostavat työnkulun.</span><span class="sxs-lookup"><span data-stu-id="003b4-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="003b4-105">Työnkulku koostuu elementeistä.</span><span class="sxs-lookup"><span data-stu-id="003b4-105">A workflow consists of elements.</span></span> <span data-ttu-id="003b4-106">Seuraavissa osissa kuvataan kutakin elementtityyppiä.</span><span class="sxs-lookup"><span data-stu-id="003b4-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="003b4-107">Tehtävät</span><span class="sxs-lookup"><span data-stu-id="003b4-107">Tasks</span></span>
<span data-ttu-id="003b4-108">*Tehtävä* on työyksikkö, joka on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="003b4-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="003b4-109">Työnkulkuun voidaan lisätä kahdentyyppisiä tehtäviä: manuaalisia ja automaattisia.</span><span class="sxs-lookup"><span data-stu-id="003b4-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="003b4-110">Manuaalinen tehtävä</span><span class="sxs-lookup"><span data-stu-id="003b4-110">Manual task</span></span>

<span data-ttu-id="003b4-111">*Manuaalinen tehtävä* on työyksikkö, joka käyttäjän on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="003b4-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="003b4-112">Esimerkiksi kuluraporttityönkulussa voi olla manuaalisia tehtäviä, joille määritettyjen käyttäjien on tehtävä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="003b4-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="003b4-113">Tarkistaa vastaanotot, jotka lähetetään kuluraportin kanssa.</span><span class="sxs-lookup"><span data-stu-id="003b4-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="003b4-114">Ottaa yhteyttä esimieheen.</span><span class="sxs-lookup"><span data-stu-id="003b4-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="003b4-115">Automaattinen tehtävä</span><span class="sxs-lookup"><span data-stu-id="003b4-115">Automated task</span></span>

<span data-ttu-id="003b4-116">*Automaattinen tehtävä* on työyksikkö, jonka järjestelmä suorittaa.</span><span class="sxs-lookup"><span data-stu-id="003b4-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="003b4-117">Käyttäjän toimia ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="003b4-117">No human interaction is required.</span></span> <span data-ttu-id="003b4-118">Esimerkiksi myyntitilaustyönkulussa voi olla automaattisia tehtäviä, joille järjestelmän on tehtävä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="003b4-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="003b4-119">Suorittaa luottorajan tarkistus.</span><span class="sxs-lookup"><span data-stu-id="003b4-119">Perform a credit check.</span></span>
-   <span data-ttu-id="003b4-120">Luoda asiakastietue asiakkaalle, jos tietuetta ei vielä ole.</span><span class="sxs-lookup"><span data-stu-id="003b4-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="003b4-121">Hyväksyntäprosessit</span><span class="sxs-lookup"><span data-stu-id="003b4-121">Approval processes</span></span>
<span data-ttu-id="003b4-122">*Hyväksyntäprosessi* koostuu erilaisista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="003b4-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="003b4-123">Hyväksyntäprosessin eri vaiheissa käyttäjä voi tehdä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="003b4-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="003b4-124">Tiedoston hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="003b4-124">Approve the document.</span></span>
-   <span data-ttu-id="003b4-125">Tiedoston hylkääminen.</span><span class="sxs-lookup"><span data-stu-id="003b4-125">Reject the document.</span></span>
-   <span data-ttu-id="003b4-126">Muutospyyntö.</span><span class="sxs-lookup"><span data-stu-id="003b4-126">Request a change to the document.</span></span>
-   <span data-ttu-id="003b4-127">Tiedoston siirtäminen toisen käyttäjän hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="003b4-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="003b4-128">Rivinimikkeen työnkulun elementit:</span><span class="sxs-lookup"><span data-stu-id="003b4-128">Lineitem workflow elements</span></span>
<span data-ttu-id="003b4-129">Työnkulku voidaan luoda käsittelemään tiedostoja tai sen rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="003b4-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="003b4-130">Oletetaan esimerkiksi, että olet luonut aikaraporttien hyväksymistyönkulun.</span><span class="sxs-lookup"><span data-stu-id="003b4-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="003b4-131">(Siihen viitataan *asiakirjan työnkulkuna*.) Voit lisätä *rivinimikkeen työnkulun* elementin kyseiseen asiakirjan työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="003b4-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="003b4-132">Rivinimikkeen elementtiä suoritettaessa kukin asiakirjan rivinimike lähetetään käsiteltäväksi.</span><span class="sxs-lookup"><span data-stu-id="003b4-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="003b4-133">Voit määrittää, käsitteleekö sama rivinimikkeiden työnkulku kaikki rivinimikkeet, tai määrittää rivinimikkeille omat rivinimikkeen työnkulut.</span><span class="sxs-lookup"><span data-stu-id="003b4-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="003b4-134">Oletetaan, että työntekijä on lähettänyt aikaraportin, joka muistuttaa seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="003b4-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span> <span data-ttu-id="003b4-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) Tässä skenaariossa voit luoda seuraavat rivinimikkeiden työkulut:</span><span class="sxs-lookup"><span data-stu-id="003b4-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="003b4-136">**Rivinimikkeen työnkulku 1** – Työnkulkua käytetään projektitunnuksella 1111 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="003b4-136">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="003b4-137">**Rivinimikkeen työnkulku 2** – Työnkulkua käytetään projektitunnuksella 2222 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="003b4-137">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="003b4-138">**Rivinimikkeen työnkulku 3** – Työnkulkua käytetään projektitunnuksella 3333 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="003b4-138">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="003b4-139">Työnkulun ohjauksen elementit</span><span class="sxs-lookup"><span data-stu-id="003b4-139">Flowcontrol elements</span></span>
<span data-ttu-id="003b4-140">Seuraavien elementtien avulla voit suunnitella työnkulkuja, joissa on vaihtoehtoisia tai samanaikaisesti suoritettavia haaroja.</span><span class="sxs-lookup"><span data-stu-id="003b4-140">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="003b4-141">Manuaalinen päätös</span><span class="sxs-lookup"><span data-stu-id="003b4-141">Manual decision</span></span>

<span data-ttu-id="003b4-142">*Manuaalinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="003b4-142">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="003b4-143">Käyttäjän on tehtävä päätös, joka määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="003b4-143">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="003b4-144">Ehdollinen päätös</span><span class="sxs-lookup"><span data-stu-id="003b4-144">Conditional decision</span></span>

<span data-ttu-id="003b4-145">Myös *ehdollinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="003b4-145">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="003b4-146">Järjestelmä kuitenkin määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="003b4-146">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="003b4-147">Järjestelmä tekee päätöksen arvioimalla asiakirjaa ja määrittämällä, täyttääkö se tietyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="003b4-147">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="003b4-148">Rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="003b4-148">Parallel activity</span></span>

<span data-ttu-id="003b4-149">*Rinnakkainen tehtävä* on työnkulun elementti, joka sisältää vähintään kaksi työnkulun haaraa, jotka ovat käynnissä yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="003b4-149">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="003b4-150">Alityönkulku</span><span class="sxs-lookup"><span data-stu-id="003b4-150">Subworkflow</span></span>

<span data-ttu-id="003b4-151">*Alityönkulku* suoritetaan toisen työnkulun yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="003b4-151">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




