---
title: Palauta kanban-työn tila
description: Tässä menettelyssä käsitellään virheellisen kanban-työtilan palauttamista.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f9026aff0f54dd2a61cb0f35705b002a125610f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148857"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="d04f0-103">Palauta kanban-työn tila</span><span class="sxs-lookup"><span data-stu-id="d04f0-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d04f0-104">Tässä menettelyssä käsitellään virheellisen kanban-työtilan palauttamista.</span><span class="sxs-lookup"><span data-stu-id="d04f0-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="d04f0-105">Tämä on kätevää, jos koneenkäyttäjä päivittää väärän työn tai määrittää vahingossa väärän tilan.</span><span class="sxs-lookup"><span data-stu-id="d04f0-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="d04f0-106">Tässä menettelyssä kanban-työ on rekisteröidään vahingossa valmistelluksi ja tila palautetaan.</span><span class="sxs-lookup"><span data-stu-id="d04f0-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="d04f0-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="d04f0-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d04f0-108">Menettely on tarkoitettu Lean-tuotantoyrityksessä työskentelevälle tuotannon osastonvalvojalle tai koneenkäyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="d04f0-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="d04f0-109">Avaa työsolun prosessitaulu.</span><span class="sxs-lookup"><span data-stu-id="d04f0-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="d04f0-110">Siirry Prosessitöiden kanban-taulu -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="d04f0-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d04f0-111">Anna tai valitse Työsolu-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="d04f0-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="d04f0-112">Valitse työsolu 1260.</span><span class="sxs-lookup"><span data-stu-id="d04f0-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="d04f0-113">Valmistele kanban-työ</span><span class="sxs-lookup"><span data-stu-id="d04f0-113">Prepare kanban job</span></span>
1. <span data-ttu-id="d04f0-114">Valitse Valmistele.</span><span class="sxs-lookup"><span data-stu-id="d04f0-114">Click Prepare.</span></span>
    * <span data-ttu-id="d04f0-115">Jos voi valita Valmistele, koska se näkyy harmaana, valmista, että valitun kanban-työn tila Suunniteltu, minkä osoituksena on tyhjä kanban-kuvake.</span><span class="sxs-lookup"><span data-stu-id="d04f0-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="d04f0-116">Jos Valmistele epäonnistuu, varmista, että kaikki keräysluettelon materiaalit ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="d04f0-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="d04f0-117">Valitse luettelossa valmisteltu työ.</span><span class="sxs-lookup"><span data-stu-id="d04f0-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="d04f0-118">Valitse ensimmäinen juuri valmisteltu työ.</span><span class="sxs-lookup"><span data-stu-id="d04f0-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="d04f0-119">Huomaa, että työn tila on valmisteltu, minkä osoittaa kanban-kuvakkeen sisällä oleva kolmio.</span><span class="sxs-lookup"><span data-stu-id="d04f0-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="d04f0-120">Palauta valmistellun kanban-työn tila</span><span class="sxs-lookup"><span data-stu-id="d04f0-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="d04f0-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d04f0-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d04f0-122">Valitse ensimmäinen juuri valmisteltu työ.</span><span class="sxs-lookup"><span data-stu-id="d04f0-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="d04f0-123">Valitse toimintoruudussa Valmista.</span><span class="sxs-lookup"><span data-stu-id="d04f0-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="d04f0-124">Valitse Palauta tila.</span><span class="sxs-lookup"><span data-stu-id="d04f0-124">Click Revert status.</span></span>
    * <span data-ttu-id="d04f0-125">Voit käyttää vaihtoehtoisia kanban-sääntöjä seuraavissa tilanteissa: – Säännöillä on sama täydennysstrategia.</span><span class="sxs-lookup"><span data-stu-id="d04f0-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="d04f0-126">- Kummallakin säännöllä on sama tuotantovirran versio.</span><span class="sxs-lookup"><span data-stu-id="d04f0-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="d04f0-127">- Kummallekin säännölle annetaan sama tuote.</span><span class="sxs-lookup"><span data-stu-id="d04f0-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="d04f0-128">- Kummallekin säännölle on määritetty samat kanban-sääntöjen viimeistä tehtävää edeltävät tehtävät.</span><span class="sxs-lookup"><span data-stu-id="d04f0-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="d04f0-129">- Kummallekin säännölle on oltava määritettynä samat varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="d04f0-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="d04f0-130">- Käsittely-yksikön tilan on oltava Ei määritetty.</span><span class="sxs-lookup"><span data-stu-id="d04f0-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="d04f0-131">- Tapahtuma-kanbanin määrityksen on oltava sama.</span><span class="sxs-lookup"><span data-stu-id="d04f0-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="d04f0-132">Varmista, että uusi tila on Suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="d04f0-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="d04f0-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d04f0-133">Click OK.</span></span>
5. <span data-ttu-id="d04f0-134">Poista valitun rivin merkintä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d04f0-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="d04f0-135">Valitse sama työ.</span><span class="sxs-lookup"><span data-stu-id="d04f0-135">Select the same job.</span></span>  
    * <span data-ttu-id="d04f0-136">Huomaa, että kanban-työn työtilaksi on palautettu Suunniteltu, minkä osoituksena on tyhjä kanban-kuvake.</span><span class="sxs-lookup"><span data-stu-id="d04f0-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

