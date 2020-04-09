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
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a4ba39b5dbba20a58066054da2e24613381cfaa
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144428"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="8b6f9-103">Luo ja määritä kustannusten kohdistuksen käytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="8b6f9-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b6f9-104">Tämän menettelyn avulla luodaan ja delegoidaan kustannusten kohdistuskäytäntö ja kustannusseurantayksikön vastaavat säännöt.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="8b6f9-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8b6f9-106">Käytännön luominen</span><span class="sxs-lookup"><span data-stu-id="8b6f9-106">Create a policy</span></span>
1. <span data-ttu-id="8b6f9-107">Valitse Kustannuslaskenta > Käytännöt > Kustannusten kohdistuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="8b6f9-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-108">Click New.</span></span>
3. <span data-ttu-id="8b6f9-109">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8b6f9-110">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8b6f9-111">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-111">Select Organization.</span></span>  
5. <span data-ttu-id="8b6f9-112">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="8b6f9-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="8b6f9-114">Kohdistussääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="8b6f9-114">Create allocation rules</span></span>
1. <span data-ttu-id="8b6f9-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-115">Click New.</span></span>
2. <span data-ttu-id="8b6f9-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8b6f9-117">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="8b6f9-118">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="8b6f9-119">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="8b6f9-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-120">Click New.</span></span>
7. <span data-ttu-id="8b6f9-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8b6f9-122">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="8b6f9-123">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="8b6f9-124">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="8b6f9-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-125">Click New.</span></span>
12. <span data-ttu-id="8b6f9-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8b6f9-127">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="8b6f9-128">Valitse Kustannustoiminta-kentässä Yhteensä.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="8b6f9-129">Anna tai valitse arvo Kohdistusperuste-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="8b6f9-130">Jatka, kunnes olet luonut kaikki säännöt.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="8b6f9-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="8b6f9-132">Käytännön delegoiminen kustannusseurantayksikköön</span><span class="sxs-lookup"><span data-stu-id="8b6f9-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="8b6f9-133">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="8b6f9-134">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-134">Click New.</span></span>
3. <span data-ttu-id="8b6f9-135">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8b6f9-136">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="8b6f9-137">Säännöillä on voimaantulopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-137">The rules are date-effective.</span></span> <span data-ttu-id="8b6f9-138">Käyttäjä tai järjestelmä voi määrittää säännöt vanhentuneeksi, jos säännöistä luodaan uusi versio.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="8b6f9-139">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="8b6f9-140">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8b6f9-140">Click Save.</span></span>

