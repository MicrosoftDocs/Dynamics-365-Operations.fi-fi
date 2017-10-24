--- 
title: "Siirrä aikataulutetut kanban-työt"
description: "Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="99c42-103">Siirrä aikataulutetut kanban-työt</span><span class="sxs-lookup"><span data-stu-id="99c42-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99c42-104">Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen.</span><span class="sxs-lookup"><span data-stu-id="99c42-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="99c42-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="99c42-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="99c42-106">Tämä menettely on tarkoitettu työnohjauksen esimiehelle tai tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.</span><span class="sxs-lookup"><span data-stu-id="99c42-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="99c42-107">Aikataulutettujen kanban-töiden valitseminen</span><span class="sxs-lookup"><span data-stu-id="99c42-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="99c42-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="99c42-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="99c42-109">!MtCMR!IAvaa haku valitsemalla Työsolu-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="99c42-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="99c42-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="99c42-110">áçêìõý !</span></span>
3. <span data-ttu-id="99c42-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="99c42-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="99c42-112">Valitse työsolu 1250.</span><span class="sxs-lookup"><span data-stu-id="99c42-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="99c42-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="99c42-113">Klik på Select.</span></span>
5. <span data-ttu-id="99c42-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="99c42-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="99c42-115">Tämä suodattaa työluettelon niin, että vain aikataulutetut kanban-työt näkyvät.</span><span class="sxs-lookup"><span data-stu-id="99c42-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="99c42-116">Kanban-töiden siirtäminen toiseen kauteen</span><span class="sxs-lookup"><span data-stu-id="99c42-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="99c42-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="99c42-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="99c42-118">Valitse työ, jonka työn tila on Suunniteltu. Voit valita esimerkiksi työn, joka on aikataulutettu suoritettavaksi 20.12.2012 Suunniteltu kausi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99c42-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="99c42-119">Siirrä sitten työ edelliseen kauteen.</span><span class="sxs-lookup"><span data-stu-id="99c42-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="99c42-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="99c42-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="99c42-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="99c42-121">Klik på End.</span></span>
    * <span data-ttu-id="99c42-122">Nyt työ siirretään työluettelon loppuun, koska sitä pidetään edellisen kauden viimeisenä työnä.</span><span class="sxs-lookup"><span data-stu-id="99c42-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="99c42-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="99c42-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="99c42-124">Valitse työ, jonka työn tila on Suunniteltu. Voit valita Suunniteltu kausi -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 18.12.2012.</span><span class="sxs-lookup"><span data-stu-id="99c42-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="99c42-125">Siirrä sitten työ seuraavaan kauteen.</span><span class="sxs-lookup"><span data-stu-id="99c42-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="99c42-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="99c42-126">Klik på Next period.</span></span>
6. <span data-ttu-id="99c42-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="99c42-127">Klik på Start.</span></span>
    * <span data-ttu-id="99c42-128">Nyt työ siirretään työluettelon alkuun, koska sitä pidetään edellisen kauden ensimmäisenä työnä.</span><span class="sxs-lookup"><span data-stu-id="99c42-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="99c42-129">Tehtävä: Työn siirtäminen kauden sisällä</span><span class="sxs-lookup"><span data-stu-id="99c42-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="99c42-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="99c42-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="99c42-131">Valitse työ, jonka työn tila on Suunniteltu. Voit valita esimerkiksi toisen työn, joka on aikataulutettu suoritettavaksi 19.12.2012 Suunniteltu kausi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99c42-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="99c42-132">Siirrä sitten työtä kauden sisällä.</span><span class="sxs-lookup"><span data-stu-id="99c42-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="99c42-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="99c42-133">Klik på Forward.</span></span>
    * <span data-ttu-id="99c42-134">Huomaa, että työtä siirrettiin yksi rivi alaspäin luettelossa.</span><span class="sxs-lookup"><span data-stu-id="99c42-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="99c42-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="99c42-135">Klik på Backward.</span></span>
    * <span data-ttu-id="99c42-136">Huomaa, että työtä siirrettiin yksi rivi ylöspäin luettelossa.</span><span class="sxs-lookup"><span data-stu-id="99c42-136">Notice that the job is moved one line up on the list.</span></span>  


