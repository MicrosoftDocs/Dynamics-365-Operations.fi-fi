---
title: Luo ja määritä kustannusten jakokäytäntö kustannusten hallinnan yksikköön
description: Kustannusten jaon sääntöjä käytetään sellaisten kustannusten jaossa, jotka on laskettu rahoituksellisesti yhteisessä kustannuspaikassa.
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
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841318"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="3bc50-103">Luo ja määritä kustannusten jakokäytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="3bc50-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3bc50-104">Kustannusten jaon sääntöjä käytetään sellaisten kustannusten jaossa, jotka on laskettu rahoituksellisesti yhteisessä kustannuspaikassa.</span><span class="sxs-lookup"><span data-stu-id="3bc50-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="3bc50-105">Kustannuslaskija varmistaa, että kustannus jaetaan kustannuspaikkoihin valitun kohdistusperusteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3bc50-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="3bc50-106">Käytäntö ja vastaavat säännöt delegoidaan kustannusseurantayksikölle.</span><span class="sxs-lookup"><span data-stu-id="3bc50-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="3bc50-107">Tämän tehtäväoppaan esimerkissä kerrotaan, miten kustannusten jaon käytäntö ja vastaavat säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="3bc50-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="3bc50-108">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="3bc50-108">Create a policy</span></span>
1. <span data-ttu-id="3bc50-109">Valitse Kustannuslaskenta > Käytännöt > Kustannusten jaon käytännöt.</span><span class="sxs-lookup"><span data-stu-id="3bc50-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="3bc50-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3bc50-110">Click New.</span></span>
3. <span data-ttu-id="3bc50-111">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3bc50-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3bc50-113">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-114">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="3bc50-114">Select Organization.</span></span>  
6. <span data-ttu-id="3bc50-115">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-116">Valitse CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="3bc50-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="3bc50-117">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-118">Valitse Jaetut tilastoelementit.</span><span class="sxs-lookup"><span data-stu-id="3bc50-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="3bc50-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3bc50-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="3bc50-120">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="3bc50-120">Create rules for the policy</span></span>
1. <span data-ttu-id="3bc50-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3bc50-121">Click New.</span></span>
2. <span data-ttu-id="3bc50-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3bc50-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3bc50-123">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-124">Laajenna hierarkia ja valitse 094.</span><span class="sxs-lookup"><span data-stu-id="3bc50-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="3bc50-125">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-126">Valitse Muut käyttökustannukset ja valitse sitten 605110 Puhdistus.</span><span class="sxs-lookup"><span data-stu-id="3bc50-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="3bc50-127">Valitse vaihtoehto Kustannustoiminta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3bc50-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="3bc50-128">Valitse Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="3bc50-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="3bc50-129">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="3bc50-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3bc50-130">Click New.</span></span>
8. <span data-ttu-id="3bc50-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3bc50-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3bc50-132">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-133">Laajenna hierarkia ja valitse 094.</span><span class="sxs-lookup"><span data-stu-id="3bc50-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="3bc50-134">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3bc50-135">Valitse Muut käyttökustannukset ja valitse sitten 605150 Vuokra.</span><span class="sxs-lookup"><span data-stu-id="3bc50-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="3bc50-136">Valitse vaihtoehto Kustannustoiminta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3bc50-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="3bc50-137">Valitse Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="3bc50-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="3bc50-138">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="3bc50-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3bc50-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="3bc50-140">Sääntöjen delegoiminen kustannusseurantayksikölle</span><span class="sxs-lookup"><span data-stu-id="3bc50-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="3bc50-141">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="3bc50-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="3bc50-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3bc50-142">Click New.</span></span>
3. <span data-ttu-id="3bc50-143">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3bc50-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3bc50-144">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3bc50-145">Valitse sallitun tilikauden syyskuu 1.</span><span class="sxs-lookup"><span data-stu-id="3bc50-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="3bc50-146">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3bc50-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="3bc50-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3bc50-147">Click Save.</span></span>

