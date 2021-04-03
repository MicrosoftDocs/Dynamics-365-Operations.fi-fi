---
title: Päivitä kanbanin tila
description: Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252819"
---
# <a name="update-kanban-status"></a><span data-ttu-id="87b89-103">Päivitä kanbanin tila</span><span class="sxs-lookup"><span data-stu-id="87b89-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87b89-104">Kun kanban tyhjennetään vahingossa tai vastaanotettu kanban on tyhjennettävä, kanbanin tila tulee päivittää.</span><span class="sxs-lookup"><span data-stu-id="87b89-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="87b89-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="87b89-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="87b89-106">Tämä menettely on tarkoitettu tuotannon työnjohtajalle.</span><span class="sxs-lookup"><span data-stu-id="87b89-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="87b89-107">Paikanna kanban.</span><span class="sxs-lookup"><span data-stu-id="87b89-107">Find the kanban.</span></span>
1. <span data-ttu-id="87b89-108">Valitse Tuotannonhallinta > Kanban > Kanbanit.</span><span class="sxs-lookup"><span data-stu-id="87b89-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="87b89-109">Avaa materiaalin käsittely-yksikön tilasarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="87b89-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="87b89-110">Valitse Tyhjennä.</span><span class="sxs-lookup"><span data-stu-id="87b89-110">Click Clear.</span></span>
    * <span data-ttu-id="87b89-111">Tämä palauttaa suodattimet.</span><span class="sxs-lookup"><span data-stu-id="87b89-111">This resets the filters.</span></span>  
4. <span data-ttu-id="87b89-112">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="87b89-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="87b89-113">Voit esimerkiksi suodattaa Kortin numero -kenttää arvolla 000149.</span><span class="sxs-lookup"><span data-stu-id="87b89-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="87b89-114">Vaihda tila tyhjennetystä vastaanotetuksi.</span><span class="sxs-lookup"><span data-stu-id="87b89-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="87b89-115">Napsauta Palauta tyhjä materiaalin käsittely-yksikkö -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="87b89-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="87b89-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="87b89-116">Click OK.</span></span>
    * <span data-ttu-id="87b89-117">Huomaa, että materiaalin käsittely-yksikön tila on Vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="87b89-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="87b89-118">Vaihda tila vastaanotetusta tyhjennetyksi.</span><span class="sxs-lookup"><span data-stu-id="87b89-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="87b89-119">Napsauta Tyhjennä kanban -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="87b89-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="87b89-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="87b89-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="87b89-121">Huomaa, että materiaalin käsittely-yksikön tila on Tyhjennetty.</span><span class="sxs-lookup"><span data-stu-id="87b89-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]