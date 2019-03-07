---
title: Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön
description: Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 92f41eb99b84bbc596e79b413971f9d92f2555b6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "324396"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="c1b7c-103">Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="c1b7c-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1b7c-104">Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="c1b7c-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c1b7c-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="c1b7c-106">Create a policy</span></span>
1. <span data-ttu-id="c1b7c-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten kohdistuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="c1b7c-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-108">Click New.</span></span>
3. <span data-ttu-id="c1b7c-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c1b7c-110">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c1b7c-111">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-111">Select Organization.</span></span>  
5. <span data-ttu-id="c1b7c-112">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="c1b7c-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="c1b7c-114">Kohdistussääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="c1b7c-114">Create allocation rules</span></span>
1. <span data-ttu-id="c1b7c-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-115">Click New.</span></span>
2. <span data-ttu-id="c1b7c-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c1b7c-117">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="c1b7c-118">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="c1b7c-119">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="c1b7c-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-120">Click New.</span></span>
7. <span data-ttu-id="c1b7c-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c1b7c-122">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="c1b7c-123">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="c1b7c-124">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="c1b7c-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-125">Click New.</span></span>
12. <span data-ttu-id="c1b7c-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c1b7c-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="c1b7c-128">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="c1b7c-129">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="c1b7c-130">Jatka, kunnes olet luonut kaikki säännöt.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="c1b7c-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="c1b7c-132">Käytännön delegoiminen kustannusseurantayksikköön</span><span class="sxs-lookup"><span data-stu-id="c1b7c-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="c1b7c-133">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="c1b7c-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-134">Click New.</span></span>
3. <span data-ttu-id="c1b7c-135">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c1b7c-136">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="c1b7c-137">Säännöillä on voimaantulopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-137">The rules are date-effective.</span></span> <span data-ttu-id="c1b7c-138">Käyttäjä tai järjestelmä voi määrittää säännöt vanhentuneeksi, jos säännöistä luodaan uusi versio.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="c1b7c-139">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="c1b7c-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c1b7c-140">Click Save.</span></span>

