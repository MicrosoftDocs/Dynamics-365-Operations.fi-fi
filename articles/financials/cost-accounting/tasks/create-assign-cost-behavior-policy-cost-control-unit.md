---
title: Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön
description: Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu.
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
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841366"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="4af42-103">Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="4af42-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4af42-104">Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu.</span><span class="sxs-lookup"><span data-stu-id="4af42-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="4af42-105">Käytäntö ja vastaavat säännöt on delegoitava kustannusseurantayksikköön, jotta käytäntö astuu voimaan.</span><span class="sxs-lookup"><span data-stu-id="4af42-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="4af42-106">Tämän menettelyn avulla luodaan käytäntö ja delegoidaan se sitten kustannusseurantayksikköön.</span><span class="sxs-lookup"><span data-stu-id="4af42-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="4af42-107">Kustannustoiminnan hierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="4af42-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="4af42-108">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="4af42-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="4af42-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-109">Click New.</span></span>
3. <span data-ttu-id="4af42-110">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="4af42-110">Click Create.</span></span>
4. <span data-ttu-id="4af42-111">Kirjoita Dimensiohierarkian nimi -kenttään Kustannustoiminnan hierarkia.</span><span class="sxs-lookup"><span data-stu-id="4af42-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="4af42-112">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-113">Valitse Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="4af42-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="4af42-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4af42-114">Click Save.</span></span>
7. <span data-ttu-id="4af42-115">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="4af42-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="4af42-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-116">Click New.</span></span>
9. <span data-ttu-id="4af42-117">Kirjoita arvo Solmun nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4af42-118">Syötä Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="4af42-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="4af42-119">Valitse puussa Cost behavior hierarchy.</span><span class="sxs-lookup"><span data-stu-id="4af42-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="4af42-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-120">Click New.</span></span>
12. <span data-ttu-id="4af42-121">Kirjoita arvo Solmun nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="4af42-122">Syötä Muuttuva kustannus.</span><span class="sxs-lookup"><span data-stu-id="4af42-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="4af42-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4af42-123">Click Save.</span></span>
14. <span data-ttu-id="4af42-124">Valitse puussa Cost behavior hierarchy\Fixed cost.</span><span class="sxs-lookup"><span data-stu-id="4af42-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="4af42-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-125">Click New.</span></span>
16. <span data-ttu-id="4af42-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4af42-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="4af42-127">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-128">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="4af42-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="4af42-129">Syötä tai valitse arvo Kohdedimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-130">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="4af42-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="4af42-131">Valitse puussa Cost behavior hierarchy\Variable cost.</span><span class="sxs-lookup"><span data-stu-id="4af42-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="4af42-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-132">Click New.</span></span>
21. <span data-ttu-id="4af42-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4af42-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="4af42-134">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-135">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="4af42-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="4af42-136">Syötä tai valitse arvo Kohdedimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-137">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="4af42-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="4af42-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4af42-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="4af42-139">Käytännön ja sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="4af42-139">Create the policy and rules</span></span>
1. <span data-ttu-id="4af42-140">Valitse Kustannuslaskenta > Käytännöt > Kustannustoiminnan käytännöt.</span><span class="sxs-lookup"><span data-stu-id="4af42-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="4af42-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-141">Click New.</span></span>
3. <span data-ttu-id="4af42-142">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4af42-143">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-144">Valitse äsken luotu käytäntöhierarkia.</span><span class="sxs-lookup"><span data-stu-id="4af42-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="4af42-145">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-146">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="4af42-146">Select Organization.</span></span>  
6. <span data-ttu-id="4af42-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4af42-147">Click Save.</span></span>
7. <span data-ttu-id="4af42-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-148">Click New.</span></span>
8. <span data-ttu-id="4af42-149">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4af42-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4af42-150">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-151">Laajenna hierarkia ja valitse Muuttuva kustannus.</span><span class="sxs-lookup"><span data-stu-id="4af42-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="4af42-152">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4af42-153">Oletusarvoisesti muuttuva prosenttiosuus on 100.</span><span class="sxs-lookup"><span data-stu-id="4af42-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="4af42-154">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="4af42-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="4af42-155">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4af42-155">Click New.</span></span>
13. <span data-ttu-id="4af42-156">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4af42-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4af42-157">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="4af42-158">Säännöillä on voimaantulopäivämäärä. Käyttäjä tai järjestelmä voi määrittää säännön vanhentuneeksi, jos säännöstä luodaan uusi versio.</span><span class="sxs-lookup"><span data-stu-id="4af42-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="4af42-159">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4af42-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="4af42-160">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4af42-160">Click Save.</span></span>

