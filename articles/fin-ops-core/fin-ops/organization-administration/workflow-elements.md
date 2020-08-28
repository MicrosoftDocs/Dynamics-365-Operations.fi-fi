---
title: Työnkulun elementit
description: Tässä ohjeaiheessa kuvataan eri osia, jotka muodostavat työnkulun.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4b0c3ee996dfbf0904f8e7fd3b3bfb53a149c2
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698044"
---
# <a name="workflow-elements"></a><span data-ttu-id="0c972-103">Työnkulun elementit</span><span class="sxs-lookup"><span data-stu-id="0c972-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c972-104">Tässä ohjeaiheessa kuvataan eri osia, jotka muodostavat työnkulun.</span><span class="sxs-lookup"><span data-stu-id="0c972-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="0c972-105">Työnkulku koostuu elementeistä.</span><span class="sxs-lookup"><span data-stu-id="0c972-105">A workflow consists of elements.</span></span> <span data-ttu-id="0c972-106">Seuraavissa osissa kuvataan kutakin elementtityyppiä.</span><span class="sxs-lookup"><span data-stu-id="0c972-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="0c972-107">Tehtävät</span><span class="sxs-lookup"><span data-stu-id="0c972-107">Tasks</span></span>

<span data-ttu-id="0c972-108">*Tehtävä* on työyksikkö, joka on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="0c972-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="0c972-109">Työnkulkuun voidaan lisätä kahdentyyppisiä tehtäviä: manuaalisia ja automaattisia.</span><span class="sxs-lookup"><span data-stu-id="0c972-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="0c972-110">Manuaalinen tehtävä</span><span class="sxs-lookup"><span data-stu-id="0c972-110">Manual task</span></span>

<span data-ttu-id="0c972-111">*Manuaalinen tehtävä* on työyksikkö, joka käyttäjän on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="0c972-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="0c972-112">Esimerkiksi kuluraporttityönkulussa voi olla manuaalisia tehtäviä, joille määritettyjen käyttäjien on tehtävä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="0c972-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="0c972-113">Tarkistaa vastaanotot, jotka lähetetään kuluraportin kanssa.</span><span class="sxs-lookup"><span data-stu-id="0c972-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="0c972-114">Ottaa yhteyttä esimieheen.</span><span class="sxs-lookup"><span data-stu-id="0c972-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="0c972-115">Automaattinen tehtävä</span><span class="sxs-lookup"><span data-stu-id="0c972-115">Automated task</span></span>

<span data-ttu-id="0c972-116">*Automaattinen tehtävä* on työyksikkö, jonka järjestelmä suorittaa.</span><span class="sxs-lookup"><span data-stu-id="0c972-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="0c972-117">Käyttäjän toimia ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="0c972-117">No human interaction is required.</span></span> <span data-ttu-id="0c972-118">Esimerkiksi myyntitilaustyönkulussa voi olla automaattisia tehtäviä, joille järjestelmän on tehtävä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="0c972-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="0c972-119">Suorittaa luottorajan tarkistus.</span><span class="sxs-lookup"><span data-stu-id="0c972-119">Perform a credit check.</span></span>
- <span data-ttu-id="0c972-120">Luoda asiakastietue asiakkaalle, jos tietuetta ei vielä ole.</span><span class="sxs-lookup"><span data-stu-id="0c972-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="0c972-121">Hyväksyntäprosessit</span><span class="sxs-lookup"><span data-stu-id="0c972-121">Approval processes</span></span>

<span data-ttu-id="0c972-122">*Hyväksyntäprosessi* koostuu erilaisista vaiheista.</span><span class="sxs-lookup"><span data-stu-id="0c972-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="0c972-123">Hyväksyntäprosessin eri vaiheissa käyttäjä voi tehdä seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="0c972-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="0c972-124">Tiedoston hyväksyminen.</span><span class="sxs-lookup"><span data-stu-id="0c972-124">Approve the document.</span></span>
- <span data-ttu-id="0c972-125">Tiedoston hylkääminen.</span><span class="sxs-lookup"><span data-stu-id="0c972-125">Reject the document.</span></span>
- <span data-ttu-id="0c972-126">Muutospyyntö.</span><span class="sxs-lookup"><span data-stu-id="0c972-126">Request a change to the document.</span></span>
- <span data-ttu-id="0c972-127">Tiedoston siirtäminen toisen käyttäjän hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="0c972-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="0c972-128">Rivinimikkeen työnkulun elementit:</span><span class="sxs-lookup"><span data-stu-id="0c972-128">Line-item workflow elements</span></span>

<span data-ttu-id="0c972-129">Työnkulku voidaan luoda käsittelemään tiedostoja tai sen rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="0c972-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="0c972-130">Oletetaan esimerkiksi, että olet luonut aikaraporttien hyväksymistyönkulun.</span><span class="sxs-lookup"><span data-stu-id="0c972-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="0c972-131">(Siihen viitataan *asiakirjan työnkulkuna*.) Voit lisätä *rivinimikkeen työnkulun* elementin kyseiseen asiakirjan työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="0c972-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="0c972-132">Rivinimikkeen elementtiä suoritettaessa kukin asiakirjan rivinimike lähetetään käsiteltäväksi.</span><span class="sxs-lookup"><span data-stu-id="0c972-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="0c972-133">Voit määrittää, käsitteleekö sama rivinimikkeiden työnkulku kaikki rivinimikkeet, tai määrittää rivinimikkeille omat rivinimikkeen työnkulut.</span><span class="sxs-lookup"><span data-stu-id="0c972-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="0c972-134">Oletetaan, että työntekijä on lähettänyt aikaraportin, joka muistuttaa seuraavaa kuvaa.</span><span class="sxs-lookup"><span data-stu-id="0c972-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Työnkulut rivinimikkeillä](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="0c972-136">Tässä skenaariossa voit luoda seuraavat rivinimikkeen työnkulut:</span><span class="sxs-lookup"><span data-stu-id="0c972-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="0c972-137">**Rivinimikkeen työnkulku 1** – Työnkulkua käytetään projektitunnuksella 1111 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="0c972-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="0c972-138">**Rivinimikkeen työnkulku 2** – Työnkulkua käytetään projektitunnuksella 2222 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="0c972-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="0c972-139">**Rivinimikkeen työnkulku 3** – Työnkulkua käytetään projektitunnuksella 3333 varustettujen rivinimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="0c972-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="0c972-140">Työnkulun ohjauksen elementit</span><span class="sxs-lookup"><span data-stu-id="0c972-140">Flow-control elements</span></span>

<span data-ttu-id="0c972-141">Seuraavien elementtien avulla voit suunnitella työnkulkuja, joissa on vaihtoehtoisia tai samanaikaisesti suoritettavia haaroja.</span><span class="sxs-lookup"><span data-stu-id="0c972-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="0c972-142">Manuaalinen päätös</span><span class="sxs-lookup"><span data-stu-id="0c972-142">Manual decision</span></span>

<span data-ttu-id="0c972-143">*Manuaalinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="0c972-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="0c972-144">Käyttäjän on tehtävä päätös, joka määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="0c972-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="0c972-145">Ehdollinen päätös</span><span class="sxs-lookup"><span data-stu-id="0c972-145">Conditional decision</span></span>

<span data-ttu-id="0c972-146">Myös *ehdollinen päätös* on piste, jossa työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="0c972-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="0c972-147">Järjestelmä kuitenkin määrittää, kumpaa haaraa käytetään lähetetyn asiakirjan käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="0c972-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="0c972-148">Järjestelmä tekee päätöksen arvioimalla asiakirjaa ja määrittämällä, täyttääkö se tietyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="0c972-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="0c972-149">Rinnakkainen tehtävä</span><span class="sxs-lookup"><span data-stu-id="0c972-149">Parallel activity</span></span>

<span data-ttu-id="0c972-150">*Rinnakkainen tehtävä* on työnkulun elementti, joka sisältää vähintään kaksi työnkulun haaraa, jotka ovat käynnissä yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="0c972-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="0c972-151">Alityönkulku</span><span class="sxs-lookup"><span data-stu-id="0c972-151">Subworkflow</span></span>

<span data-ttu-id="0c972-152">*Alityönkulku* suoritetaan toisen työnkulun yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0c972-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
