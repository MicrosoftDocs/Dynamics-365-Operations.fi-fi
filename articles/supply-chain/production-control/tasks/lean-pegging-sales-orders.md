--- 
title: Lean-tarvekohdistus myyntitilauksista
description: "Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dbab5ade75aa8999f7e91c5d27f896242f6c7604
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="b6f74-103">Lean-tarvekohdistus myyntitilauksista</span><span class="sxs-lookup"><span data-stu-id="b6f74-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6f74-104">Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla.</span><span class="sxs-lookup"><span data-stu-id="b6f74-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="b6f74-105">Tarvekohdistuspuun vahvistamisen jälkeen kaikki kanban-työt on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="b6f74-106">Tämä on kätevää tilausskenaarioissa, joissa tilauksen vastaanottajan on varmistettava, että tuotanto voi alkaa heti.</span><span class="sxs-lookup"><span data-stu-id="b6f74-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="b6f74-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b6f74-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b6f74-108">Tämä menettely on tarkoitettu Lean-yrityksen ennakkotilausten vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="b6f74-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="b6f74-109">Luo kanban-ohjatun nimikkeen myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="b6f74-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="b6f74-110">Siirry Kaikki myyntitilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="b6f74-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="b6f74-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b6f74-111">Click New.</span></span>
3. <span data-ttu-id="b6f74-112">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b6f74-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="b6f74-113">Käytä arvoa US-001.</span><span class="sxs-lookup"><span data-stu-id="b6f74-113">Use US-001.</span></span>  
4. <span data-ttu-id="b6f74-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b6f74-114">Click OK.</span></span>
5. <span data-ttu-id="b6f74-115">Kirjoita Nimiketunnus-kenttään L0001.</span><span class="sxs-lookup"><span data-stu-id="b6f74-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="b6f74-116">Valitse määräksi 30.</span><span class="sxs-lookup"><span data-stu-id="b6f74-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="b6f74-117">On tärkeää, että määrä on suurempi kuin 24, jotta tapahtuman kanban-sääntö käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="b6f74-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="b6f74-118">Avaa tarvekohdistuspuu</span><span class="sxs-lookup"><span data-stu-id="b6f74-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="b6f74-119">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="b6f74-119">Click Product and supply.</span></span>
2. <span data-ttu-id="b6f74-120">Valitse Näytä tarvekohdistuspuu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="b6f74-121">Huomaa, että kaikki myyntitilausrivin tarvitsemat tarvekohdistustasot näkyvät tarvekohdistuspuussa.</span><span class="sxs-lookup"><span data-stu-id="b6f74-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="b6f74-122">Tässä tapauksessa näkyvissä on kaksi kanban-tasoa ja kaikki pakolliset komponentit.</span><span class="sxs-lookup"><span data-stu-id="b6f74-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="b6f74-123">Suunnittele tarvekohdistuspuu</span><span class="sxs-lookup"><span data-stu-id="b6f74-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="b6f74-124">Valitse puussa Myyntirivi 000832\Kanban 000558.</span><span class="sxs-lookup"><span data-stu-id="b6f74-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="b6f74-125">Laajenna Kanban-työt-osa.</span><span class="sxs-lookup"><span data-stu-id="b6f74-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="b6f74-126">Huomaa, että kanban-työn tila on Ei suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="b6f74-127">Valitse Suunnittele koko tarvekohdistuspuu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="b6f74-128">Tällöin kaikki kanban-työt suunnitellaan tarvekohdistuspuussa, mikä muuttaa työn tilan Ei suunniteltu tilaksi Suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="b6f74-129">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-129">Refresh the page.</span></span>
    * <span data-ttu-id="b6f74-130">Huomaa, että kanban-työn tila muuttui ei suunnitellusta suunnitelluksi.</span><span class="sxs-lookup"><span data-stu-id="b6f74-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="b6f74-131">Valitse puussa Myyntirivi 000832\Kanban 000558\Varasto-otto L0001\Kanban 000559.</span><span class="sxs-lookup"><span data-stu-id="b6f74-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="b6f74-132">Myös toisen kanbanin työ on suunniteltu, koska koko tarvekohdistuspuu on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="b6f74-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="b6f74-133">Huomaa, että kanban-työn tila on muuttunut ei suunnitellusta suunnitelluksi.</span><span class="sxs-lookup"><span data-stu-id="b6f74-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


