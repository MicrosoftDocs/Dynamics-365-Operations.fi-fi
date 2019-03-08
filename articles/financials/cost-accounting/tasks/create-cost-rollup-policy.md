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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "362599"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="76976-103">Kustannusten koontikäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="76976-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76976-104">Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="76976-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="76976-105">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="76976-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="76976-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="76976-106">Create a policy</span></span>
1. <span data-ttu-id="76976-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.</span><span class="sxs-lookup"><span data-stu-id="76976-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="76976-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76976-108">Click New.</span></span>
3. <span data-ttu-id="76976-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="76976-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76976-111">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-112">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="76976-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="76976-113">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-114">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="76976-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="76976-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="76976-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="76976-116">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="76976-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="76976-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76976-117">Click New.</span></span>
2. <span data-ttu-id="76976-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="76976-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="76976-119">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-120">Valitse 007.</span><span class="sxs-lookup"><span data-stu-id="76976-120">Select 007.</span></span>  
4. <span data-ttu-id="76976-121">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-122">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="76976-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="76976-123">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-124">Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="76976-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="76976-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76976-125">Click New.</span></span>
7. <span data-ttu-id="76976-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="76976-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="76976-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-128">Valitse 008.</span><span class="sxs-lookup"><span data-stu-id="76976-128">Select 008.</span></span>  
9. <span data-ttu-id="76976-129">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-130">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="76976-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="76976-131">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-132">Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="76976-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="76976-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76976-133">Click New.</span></span>
12. <span data-ttu-id="76976-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="76976-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="76976-135">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-136">Valitse 009.</span><span class="sxs-lookup"><span data-stu-id="76976-136">Select 009.</span></span>  
14. <span data-ttu-id="76976-137">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-138">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="76976-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="76976-139">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="76976-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="76976-140">Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="76976-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="76976-141">Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="76976-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="76976-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="76976-142">Click Save.</span></span>

