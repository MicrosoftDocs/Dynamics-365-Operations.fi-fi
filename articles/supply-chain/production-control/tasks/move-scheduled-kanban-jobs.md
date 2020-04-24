---
title: Siirrä aikataulutetut kanban-työt
description: Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb95bab2173cb45300560f59c394cd2d558fe69f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206976"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="33015-103">Siirrä aikataulutetut kanban-työt</span><span class="sxs-lookup"><span data-stu-id="33015-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33015-104">Tässä menettelyssä keskitytään prosessin suunniteltujen kanban-töiden siirtämiseen toiseen kauteen.</span><span class="sxs-lookup"><span data-stu-id="33015-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="33015-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="33015-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="33015-106">Tämä menettely on tarkoitettu työnohjauksen esimiehelle tai tuotannon suunnittelijalle, jotka käsittelevät kanbaneita.</span><span class="sxs-lookup"><span data-stu-id="33015-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="33015-107">Valitse aikataulutetut kanban-työt.</span><span class="sxs-lookup"><span data-stu-id="33015-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="33015-108">Valitse **Tuotannonhallinta > Kanban > Kanban-työn aikataulutus**.</span><span class="sxs-lookup"><span data-stu-id="33015-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="33015-109">Avaa haku valitsemalla **Työsolu**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="33015-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="33015-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="33015-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="33015-111">Valitse työsolu 1250.</span><span class="sxs-lookup"><span data-stu-id="33015-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="33015-112">Klikkaa **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="33015-112">Click **Select**.</span></span> 

5. <span data-ttu-id="33015-113">Valitse **Näytä työn tila** -kentässä **Ajoitettu**.</span><span class="sxs-lookup"><span data-stu-id="33015-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="33015-114">Tämä suodattaa työluettelon niin, että vain aikataulutetut kanban-työt näkyvät.</span><span class="sxs-lookup"><span data-stu-id="33015-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="33015-115">Siirrä kanban-työt toiseen jaksoon.</span><span class="sxs-lookup"><span data-stu-id="33015-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="33015-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33015-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="33015-117">Valitse työ, jonka työn tila on **Suunniteltu**. Voit valita, **Suunniteltu kausi** -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 20.12.2012.</span><span class="sxs-lookup"><span data-stu-id="33015-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="33015-118">Siirrä sitten työ edelliseen kauteen.</span><span class="sxs-lookup"><span data-stu-id="33015-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="33015-119">Valitse **Edellinen jakso**.</span><span class="sxs-lookup"><span data-stu-id="33015-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="33015-120">Siirrä työ työluettelon loppuun valitsemalla **Loppu**, koska sitä pidetään edellisen kauden viimeisenä työnä.</span><span class="sxs-lookup"><span data-stu-id="33015-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="33015-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33015-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="33015-122">Valitse työ, jonka työn tila on **Suunniteltu**. Voit valita **Suunniteltu kausi** -kentässä esimerkiksi työn, joka on aikataulutettu suoritettavaksi 18.12.2012.</span><span class="sxs-lookup"><span data-stu-id="33015-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="33015-123">Siirrä sitten työ seuraavaan kauteen.</span><span class="sxs-lookup"><span data-stu-id="33015-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="33015-124">Valitse **Seuraava jakso**.</span><span class="sxs-lookup"><span data-stu-id="33015-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="33015-125">Siirrä työ työluettelon alkuun valitsemalla **Alku**, koska sitä pidetään edellisen kauden ensimmäisenä työnä.</span><span class="sxs-lookup"><span data-stu-id="33015-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="33015-126">Siirrä työtä kauden sisällä.</span><span class="sxs-lookup"><span data-stu-id="33015-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="33015-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="33015-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="33015-128">Valitse työ, jonka työn tila on Suunniteltu. Voit valita **Suunniteltu kausi** -kentässä esimerkiksi toisen työn, joka on aikataulutettu suoritettavaksi 19.12.2012.</span><span class="sxs-lookup"><span data-stu-id="33015-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="33015-129">Siirrä sitten työtä kauden sisällä.</span><span class="sxs-lookup"><span data-stu-id="33015-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="33015-130">Valitse **Eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="33015-130">Click **Forward**.</span></span> <span data-ttu-id="33015-131">Huomaa, että työtä siirrettiin yksi rivi alaspäin luettelossa.</span><span class="sxs-lookup"><span data-stu-id="33015-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="33015-132">Valitse **Taaksepäin**.</span><span class="sxs-lookup"><span data-stu-id="33015-132">Click **Backward**.</span></span> <span data-ttu-id="33015-133">Huomaa, että työtä siirrettiin yksi rivi ylöspäin luettelossa.</span><span class="sxs-lookup"><span data-stu-id="33015-133">Notice that the job is moved one line up on the list.</span></span>
