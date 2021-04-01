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
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261281"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="54cff-103">Kustannusten koontikäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="54cff-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54cff-104">Tässä menettelyssä näytetään, miten kustannusten koontikäytäntö ja käytännön säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="54cff-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="54cff-105">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="54cff-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="54cff-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="54cff-106">Create a policy</span></span>
1. <span data-ttu-id="54cff-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten koontikäytännöt.</span><span class="sxs-lookup"><span data-stu-id="54cff-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="54cff-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="54cff-108">Click New.</span></span>
3. <span data-ttu-id="54cff-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="54cff-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="54cff-111">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-112">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="54cff-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="54cff-113">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-114">Valitse Kustannusten koonnin CC.</span><span class="sxs-lookup"><span data-stu-id="54cff-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="54cff-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="54cff-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="54cff-116">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="54cff-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="54cff-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="54cff-117">Click New.</span></span>
2. <span data-ttu-id="54cff-118">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54cff-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="54cff-119">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-120">Valitse 007.</span><span class="sxs-lookup"><span data-stu-id="54cff-120">Select 007.</span></span>  
4. <span data-ttu-id="54cff-121">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-122">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="54cff-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="54cff-123">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-124">Tässä esimerkissä määritetään toissijaisen kustannustason CC-007 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="54cff-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="54cff-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="54cff-125">Click New.</span></span>
7. <span data-ttu-id="54cff-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54cff-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="54cff-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-128">Valitse 008.</span><span class="sxs-lookup"><span data-stu-id="54cff-128">Select 008.</span></span>  
9. <span data-ttu-id="54cff-129">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-130">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="54cff-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="54cff-131">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-132">Tässä esimerkissä määritetään toissijaisen kustannustason CC-008 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="54cff-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="54cff-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="54cff-133">Click New.</span></span>
12. <span data-ttu-id="54cff-134">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="54cff-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="54cff-135">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-136">Valitse 009.</span><span class="sxs-lookup"><span data-stu-id="54cff-136">Select 009.</span></span>  
14. <span data-ttu-id="54cff-137">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-138">Valitse Kustannusten koonnin CE.</span><span class="sxs-lookup"><span data-stu-id="54cff-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="54cff-139">Syötä tai valitse arvo Toissijainen kustannustaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="54cff-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="54cff-140">Tässä esimerkissä määritetään toissijaisen kustannustason CC-009 ja kustannuspaikan vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="54cff-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="54cff-141">Jatka, kunnes kaikkien kustannuspaikkojen ja niiden vastaavien toissijaisten kustannustasojen vastaavuus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="54cff-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="54cff-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="54cff-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]