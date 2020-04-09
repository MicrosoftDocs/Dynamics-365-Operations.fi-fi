---
title: Lean-tarvekohdistus myyntitilauksista
description: Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5142fe552147a9b2988a8828ba1206fad9e252e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146741"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="28f1b-103">Lean-tarvekohdistus myyntitilauksista</span><span class="sxs-lookup"><span data-stu-id="28f1b-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28f1b-104">Tässä menettelyssä käsitellään sellaisen myyntirivin tarvekohdistuspuuta, jossa nimike tuotetaan kanbanien avulla.</span><span class="sxs-lookup"><span data-stu-id="28f1b-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="28f1b-105">Tarvekohdistuspuun vahvistamisen jälkeen kaikki kanban-työt on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="28f1b-106">Tämä on kätevää tilausskenaarioissa, joissa tilauksen vastaanottajan on varmistettava, että tuotanto voi alkaa heti.</span><span class="sxs-lookup"><span data-stu-id="28f1b-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="28f1b-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="28f1b-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="28f1b-108">Tämä menettely on tarkoitettu Lean-yrityksen ennakkotilausten vastaanottajille.</span><span class="sxs-lookup"><span data-stu-id="28f1b-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="28f1b-109">Luo kanban-ohjatun nimikkeen myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="28f1b-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="28f1b-110">Siirry Kaikki myyntitilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="28f1b-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="28f1b-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="28f1b-111">Click New.</span></span>
3. <span data-ttu-id="28f1b-112">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="28f1b-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="28f1b-113">Käytä arvoa US-001.</span><span class="sxs-lookup"><span data-stu-id="28f1b-113">Use US-001.</span></span>  
4. <span data-ttu-id="28f1b-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="28f1b-114">Click OK.</span></span>
5. <span data-ttu-id="28f1b-115">Kirjoita Nimiketunnus-kenttään L0001.</span><span class="sxs-lookup"><span data-stu-id="28f1b-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="28f1b-116">Valitse määräksi 30.</span><span class="sxs-lookup"><span data-stu-id="28f1b-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="28f1b-117">On tärkeää, että määrä on suurempi kuin 24, jotta tapahtuman kanban-sääntö käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="28f1b-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="28f1b-118">Avaa tarvekohdistuspuu</span><span class="sxs-lookup"><span data-stu-id="28f1b-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="28f1b-119">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="28f1b-119">Click Product and supply.</span></span>
2. <span data-ttu-id="28f1b-120">Valitse Näytä tarvekohdistuspuu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="28f1b-121">Huomaa, että kaikki myyntitilausrivin tarvitsemat tarvekohdistustasot näkyvät tarvekohdistuspuussa.</span><span class="sxs-lookup"><span data-stu-id="28f1b-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="28f1b-122">Tässä tapauksessa näkyvissä on kaksi kanban-tasoa ja kaikki pakolliset komponentit.</span><span class="sxs-lookup"><span data-stu-id="28f1b-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="28f1b-123">Suunnittele tarvekohdistuspuu</span><span class="sxs-lookup"><span data-stu-id="28f1b-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="28f1b-124">Valitse puussa Myyntirivi 000832\Kanban 000558.</span><span class="sxs-lookup"><span data-stu-id="28f1b-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="28f1b-125">Laajenna Kanban-työt-osa.</span><span class="sxs-lookup"><span data-stu-id="28f1b-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="28f1b-126">Huomaa, että kanban-työn tila on Ei suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="28f1b-127">Valitse Suunnittele koko tarvekohdistuspuu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="28f1b-128">Tällöin kaikki kanban-työt suunnitellaan tarvekohdistuspuussa, mikä muuttaa työn tilan Ei suunniteltu tilaksi Suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="28f1b-129">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-129">Refresh the page.</span></span>
    * <span data-ttu-id="28f1b-130">Huomaa, että kanban-työn tila muuttui ei suunnitellusta suunnitelluksi.</span><span class="sxs-lookup"><span data-stu-id="28f1b-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="28f1b-131">Valitse puussa Myyntirivi 000832\Kanban 000558\Varasto-otto L0001\Kanban 000559.</span><span class="sxs-lookup"><span data-stu-id="28f1b-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="28f1b-132">Myös toisen kanbanin työ on suunniteltu, koska koko tarvekohdistuspuu on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="28f1b-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="28f1b-133">Huomaa, että kanban-työn tila on muuttunut ei suunnitellusta suunnitelluksi.</span><span class="sxs-lookup"><span data-stu-id="28f1b-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

