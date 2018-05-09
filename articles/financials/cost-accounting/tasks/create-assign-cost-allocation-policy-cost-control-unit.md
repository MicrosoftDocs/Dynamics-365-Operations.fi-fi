--- 
title: "Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön"
description: "Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 754b5e46c0060b9252fb5b0cc361619ef2a9c695
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="62535-103">Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="62535-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62535-104">Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt.</span><span class="sxs-lookup"><span data-stu-id="62535-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="62535-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="62535-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="62535-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="62535-106">Create a policy</span></span>
1. <span data-ttu-id="62535-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten kohdistuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="62535-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="62535-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62535-108">Click New.</span></span>
3. <span data-ttu-id="62535-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="62535-110">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="62535-111">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="62535-111">Select Organization.</span></span>  
5. <span data-ttu-id="62535-112">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="62535-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="62535-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="62535-114">Kohdistussääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="62535-114">Create allocation rules</span></span>
1. <span data-ttu-id="62535-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62535-115">Click New.</span></span>
2. <span data-ttu-id="62535-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="62535-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="62535-117">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="62535-118">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="62535-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="62535-119">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="62535-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62535-120">Click New.</span></span>
7. <span data-ttu-id="62535-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="62535-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="62535-122">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="62535-123">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="62535-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="62535-124">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="62535-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62535-125">Click New.</span></span>
12. <span data-ttu-id="62535-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="62535-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="62535-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="62535-128">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="62535-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="62535-129">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="62535-130">Jatka, kunnes olet luonut kaikki säännöt.</span><span class="sxs-lookup"><span data-stu-id="62535-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="62535-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="62535-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="62535-132">Käytännön delegoiminen kustannusseurantayksikköön</span><span class="sxs-lookup"><span data-stu-id="62535-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="62535-133">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="62535-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="62535-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="62535-134">Click New.</span></span>
3. <span data-ttu-id="62535-135">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="62535-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="62535-136">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="62535-137">Säännöillä on voimaantulopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="62535-137">The rules are date-effective.</span></span> <span data-ttu-id="62535-138">Käyttäjä tai järjestelmä voi määrittää säännöt vanhentuneeksi, jos säännöistä luodaan uusi versio.</span><span class="sxs-lookup"><span data-stu-id="62535-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="62535-139">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="62535-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="62535-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="62535-140">Click Save.</span></span>


