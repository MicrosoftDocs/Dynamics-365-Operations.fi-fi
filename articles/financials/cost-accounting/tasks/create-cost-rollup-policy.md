---
title: Kustannusten koontikäytännön luominen
description: Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841222"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="36d70-103">Kustannusten koontikäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="36d70-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36d70-104">Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="36d70-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="36d70-105">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="36d70-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="36d70-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="36d70-106">Create a policy</span></span>
1. <span data-ttu-id="36d70-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.</span><span class="sxs-lookup"><span data-stu-id="36d70-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="36d70-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36d70-108">Click New.</span></span>
3. <span data-ttu-id="36d70-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="36d70-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="36d70-111">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-112">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="36d70-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="36d70-113">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-114">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="36d70-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="36d70-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36d70-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="36d70-116">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="36d70-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="36d70-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36d70-117">Click New.</span></span>
2. <span data-ttu-id="36d70-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36d70-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="36d70-119">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-120">Valitse 007.</span><span class="sxs-lookup"><span data-stu-id="36d70-120">Select 007.</span></span>  
4. <span data-ttu-id="36d70-121">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-122">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="36d70-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="36d70-123">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-124">Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="36d70-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="36d70-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36d70-125">Click New.</span></span>
7. <span data-ttu-id="36d70-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36d70-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="36d70-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-128">Valitse 008.</span><span class="sxs-lookup"><span data-stu-id="36d70-128">Select 008.</span></span>  
9. <span data-ttu-id="36d70-129">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-130">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="36d70-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="36d70-131">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-132">Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="36d70-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="36d70-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="36d70-133">Click New.</span></span>
12. <span data-ttu-id="36d70-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="36d70-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="36d70-135">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-136">Valitse 009.</span><span class="sxs-lookup"><span data-stu-id="36d70-136">Select 009.</span></span>  
14. <span data-ttu-id="36d70-137">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-138">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="36d70-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="36d70-139">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="36d70-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="36d70-140">Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="36d70-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="36d70-141">Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="36d70-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="36d70-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="36d70-142">Click Save.</span></span>

