---
title: Päivitä kanbanin tila
description: Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d069414829518c8c952a0e7a74cd0ae4f24c450
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571378"
---
# <a name="update-kanban-status"></a><span data-ttu-id="14557-103">Päivitä kanbanin tila</span><span class="sxs-lookup"><span data-stu-id="14557-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14557-104">Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.</span><span class="sxs-lookup"><span data-stu-id="14557-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="14557-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="14557-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="14557-106">Tämä menettely on tarkoitettu tuotannon työnjohtajalle.</span><span class="sxs-lookup"><span data-stu-id="14557-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="14557-107">Paikanna kanban.</span><span class="sxs-lookup"><span data-stu-id="14557-107">Find the kanban.</span></span>
1. <span data-ttu-id="14557-108">Valitse Tuotannonhallinta > Kanban > Kanbanit.</span><span class="sxs-lookup"><span data-stu-id="14557-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="14557-109">Avaa materiaalin käsittely-yksikön tilasarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="14557-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="14557-110">Valitse Tyhjennä.</span><span class="sxs-lookup"><span data-stu-id="14557-110">Click Clear.</span></span>
    * <span data-ttu-id="14557-111">Tämä palauttaa suodattimet.</span><span class="sxs-lookup"><span data-stu-id="14557-111">This resets the filters.</span></span>  
4. <span data-ttu-id="14557-112">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="14557-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="14557-113">Voit esimerkiksi suodattaa Kortin numero -kenttää arvolla 000149.</span><span class="sxs-lookup"><span data-stu-id="14557-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="14557-114">Vaihda tila tyhjennetystä vastaanotetuksi.</span><span class="sxs-lookup"><span data-stu-id="14557-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="14557-115">Napsauta Palauta tyhjä materiaalin käsittely-yksikkö -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="14557-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="14557-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="14557-116">Click OK.</span></span>
    * <span data-ttu-id="14557-117">Huomaa, että materiaalin käsittely-yksikön tila on Vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="14557-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="14557-118">Vaihda tila vastaanotetusta tyhjennetyksi.</span><span class="sxs-lookup"><span data-stu-id="14557-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="14557-119">Napsauta Tyhjennä kanban -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="14557-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="14557-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="14557-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="14557-121">Huomaa, että materiaalin käsittely-yksikön tila on Tyhjennetty.</span><span class="sxs-lookup"><span data-stu-id="14557-121">Notice that the Handling unit status is Emptied.</span></span>  

