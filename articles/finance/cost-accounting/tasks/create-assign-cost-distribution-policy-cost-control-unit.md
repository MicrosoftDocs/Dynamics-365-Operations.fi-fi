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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177538"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="dd702-103">Luo ja määritä kustannusten jakokäytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="dd702-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd702-104">Kustannusten jaon sääntöjä käytetään sellaisten kustannusten jaossa, jotka on laskettu rahoituksellisesti yhteisessä kustannuspaikassa.</span><span class="sxs-lookup"><span data-stu-id="dd702-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="dd702-105">Kustannuslaskija varmistaa, että kustannus jaetaan kustannuspaikkoihin valitun kohdistusperusteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="dd702-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="dd702-106">Käytäntö ja vastaavat säännöt delegoidaan kustannusseurantayksikölle.</span><span class="sxs-lookup"><span data-stu-id="dd702-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="dd702-107">Tämän tehtäväoppaan esimerkissä kerrotaan, miten kustannusten jaon käytäntö ja vastaavat säännöt luodaan.</span><span class="sxs-lookup"><span data-stu-id="dd702-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="dd702-108">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="dd702-108">Create a policy</span></span>
1. <span data-ttu-id="dd702-109">Valitse Kustannuslaskenta > Käytännöt > Kustannusten jaon käytännöt.</span><span class="sxs-lookup"><span data-stu-id="dd702-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="dd702-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dd702-110">Click New.</span></span>
3. <span data-ttu-id="dd702-111">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="dd702-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dd702-113">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-114">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="dd702-114">Select Organization.</span></span>  
6. <span data-ttu-id="dd702-115">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-116">Valitse CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="dd702-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="dd702-117">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-118">Valitse Jaetut tilastoelementit.</span><span class="sxs-lookup"><span data-stu-id="dd702-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="dd702-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="dd702-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="dd702-120">Käytännön sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="dd702-120">Create rules for the policy</span></span>
1. <span data-ttu-id="dd702-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dd702-121">Click New.</span></span>
2. <span data-ttu-id="dd702-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dd702-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="dd702-123">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-124">Laajenna hierarkia ja valitse 094.</span><span class="sxs-lookup"><span data-stu-id="dd702-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="dd702-125">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-126">Valitse Muut käyttökustannukset ja valitse sitten 605110 Puhdistus.</span><span class="sxs-lookup"><span data-stu-id="dd702-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="dd702-127">Valitse vaihtoehto Kustannustoiminta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dd702-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="dd702-128">Valitse Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="dd702-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="dd702-129">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="dd702-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dd702-130">Click New.</span></span>
8. <span data-ttu-id="dd702-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dd702-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dd702-132">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-133">Laajenna hierarkia ja valitse 094.</span><span class="sxs-lookup"><span data-stu-id="dd702-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="dd702-134">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dd702-135">Valitse Muut käyttökustannukset ja valitse sitten 605150 Vuokra.</span><span class="sxs-lookup"><span data-stu-id="dd702-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="dd702-136">Valitse vaihtoehto Kustannustoiminta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dd702-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="dd702-137">Valitse Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="dd702-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="dd702-138">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="dd702-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="dd702-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="dd702-140">Sääntöjen delegoiminen kustannusseurantayksikölle</span><span class="sxs-lookup"><span data-stu-id="dd702-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="dd702-141">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="dd702-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="dd702-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dd702-142">Click New.</span></span>
3. <span data-ttu-id="dd702-143">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dd702-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dd702-144">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="dd702-145">Valitse sallitun tilikauden syyskuu 1.</span><span class="sxs-lookup"><span data-stu-id="dd702-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="dd702-146">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dd702-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="dd702-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="dd702-147">Click Save.</span></span>
