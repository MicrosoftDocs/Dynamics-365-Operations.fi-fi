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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0a648984a8b4aaa314707e72a615f516116a193
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990739"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="75a2e-103">Kustannusten koontikäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="75a2e-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75a2e-104">Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="75a2e-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="75a2e-105">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="75a2e-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="75a2e-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="75a2e-106">Create a policy</span></span>
1. <span data-ttu-id="75a2e-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.</span><span class="sxs-lookup"><span data-stu-id="75a2e-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="75a2e-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="75a2e-108">Click New.</span></span>
3. <span data-ttu-id="75a2e-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="75a2e-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="75a2e-111">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-112">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="75a2e-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="75a2e-113">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-114">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="75a2e-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="75a2e-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="75a2e-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="75a2e-116">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="75a2e-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="75a2e-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="75a2e-117">Click New.</span></span>
2. <span data-ttu-id="75a2e-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="75a2e-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="75a2e-119">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-120">Valitse 007.</span><span class="sxs-lookup"><span data-stu-id="75a2e-120">Select 007.</span></span>  
4. <span data-ttu-id="75a2e-121">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-122">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="75a2e-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="75a2e-123">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-124">Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="75a2e-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="75a2e-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="75a2e-125">Click New.</span></span>
7. <span data-ttu-id="75a2e-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="75a2e-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="75a2e-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-128">Valitse 008.</span><span class="sxs-lookup"><span data-stu-id="75a2e-128">Select 008.</span></span>  
9. <span data-ttu-id="75a2e-129">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-130">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="75a2e-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="75a2e-131">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-132">Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="75a2e-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="75a2e-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="75a2e-133">Click New.</span></span>
12. <span data-ttu-id="75a2e-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="75a2e-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="75a2e-135">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-136">Valitse 009.</span><span class="sxs-lookup"><span data-stu-id="75a2e-136">Select 009.</span></span>  
14. <span data-ttu-id="75a2e-137">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-138">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="75a2e-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="75a2e-139">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="75a2e-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="75a2e-140">Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="75a2e-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="75a2e-141">Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="75a2e-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="75a2e-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="75a2e-142">Click Save.</span></span>

