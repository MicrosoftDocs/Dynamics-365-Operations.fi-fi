--- 
title: "Päivitä kanbanin tila"
description: "Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="update-kanban-status"></a><span data-ttu-id="cc2f2-103">Päivitä kanbanin tila</span><span class="sxs-lookup"><span data-stu-id="cc2f2-103">Update kanban status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc2f2-104">Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="cc2f2-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cc2f2-106">Tämä menettely on tarkoitettu tuotannon työnjohtajalle.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="cc2f2-107">Paikanna kanban.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-107">Find the kanban.</span></span>
1. <span data-ttu-id="cc2f2-108">Valitse Tuotannonhallinta > Kanban > Kanbanit.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="cc2f2-109">Avaa materiaalin käsittely-yksikön tilasarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="cc2f2-110">Valitse Tyhjennä.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-110">Click Clear.</span></span>
    * <span data-ttu-id="cc2f2-111">Tämä palauttaa suodattimet.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-111">This resets the filters.</span></span>  
4. <span data-ttu-id="cc2f2-112">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cc2f2-113">Voit esimerkiksi suodattaa Kortin numero -kenttää arvolla 000149.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="cc2f2-114">Vaihda tila tyhjennetystä vastaanotetuksi.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="cc2f2-115">Napsauta Palauta tyhjä materiaalin käsittely-yksikkö -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="cc2f2-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-116">Click OK.</span></span>
    * <span data-ttu-id="cc2f2-117">Huomaa, että materiaalin käsittely-yksikön tila on Vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="cc2f2-118">Vaihda tila vastaanotetusta tyhjennetyksi.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="cc2f2-119">Napsauta Tyhjennä kanban -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="cc2f2-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cc2f2-121">Huomaa, että materiaalin käsittely-yksikön tila on Tyhjennetty.</span><span class="sxs-lookup"><span data-stu-id="cc2f2-121">Notice that the Handling unit status is Emptied.</span></span>  


