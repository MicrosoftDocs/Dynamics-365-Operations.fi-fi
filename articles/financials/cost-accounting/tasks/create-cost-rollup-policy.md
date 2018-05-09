--- 
title: "Kustannusten koontikäytännön luominen"
description: "Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e6eddaf80d7b508a2d477bdd731b2b19cb02acd5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="97aeb-103">Kustannusten koontikäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="97aeb-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97aeb-104">Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="97aeb-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="97aeb-105">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="97aeb-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="97aeb-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="97aeb-106">Create a policy</span></span>
1. <span data-ttu-id="97aeb-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.</span><span class="sxs-lookup"><span data-stu-id="97aeb-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="97aeb-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aeb-108">Click New.</span></span>
3. <span data-ttu-id="97aeb-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="97aeb-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97aeb-111">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-112">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="97aeb-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="97aeb-113">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-114">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="97aeb-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="97aeb-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="97aeb-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="97aeb-116">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="97aeb-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="97aeb-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aeb-117">Click New.</span></span>
2. <span data-ttu-id="97aeb-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="97aeb-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="97aeb-119">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-120">Valitse 007.</span><span class="sxs-lookup"><span data-stu-id="97aeb-120">Select 007.</span></span>  
4. <span data-ttu-id="97aeb-121">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-122">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="97aeb-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="97aeb-123">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-124">Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="97aeb-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="97aeb-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aeb-125">Click New.</span></span>
7. <span data-ttu-id="97aeb-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="97aeb-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="97aeb-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-128">Valitse 008.</span><span class="sxs-lookup"><span data-stu-id="97aeb-128">Select 008.</span></span>  
9. <span data-ttu-id="97aeb-129">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-130">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="97aeb-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="97aeb-131">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-132">Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="97aeb-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="97aeb-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aeb-133">Click New.</span></span>
12. <span data-ttu-id="97aeb-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="97aeb-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="97aeb-135">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-136">Valitse 009.</span><span class="sxs-lookup"><span data-stu-id="97aeb-136">Select 009.</span></span>  
14. <span data-ttu-id="97aeb-137">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-138">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="97aeb-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="97aeb-139">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aeb-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="97aeb-140">Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="97aeb-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="97aeb-141">Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="97aeb-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="97aeb-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="97aeb-142">Click Save.</span></span>


