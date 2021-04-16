---
title: Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön
description: Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757e5a5be94e7190f4dbb51d667dc8adec4b824a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826320"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="7b53b-103">Luo ja määritä kustannustoimintakäytäntö kustannusten hallinnan yksikköön</span><span class="sxs-lookup"><span data-stu-id="7b53b-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b53b-104">Kustannustoiminta on sekä kiinteiden että muuttuvien kustannusten luokittelu.</span><span class="sxs-lookup"><span data-stu-id="7b53b-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="7b53b-105">Käytäntö ja vastaavat säännöt on delegoitava kustannusseurantayksikköön, jotta käytäntö astuu voimaan.</span><span class="sxs-lookup"><span data-stu-id="7b53b-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="7b53b-106">Tämän menettelyn avulla luodaan käytäntö ja delegoidaan se sitten kustannusseurantayksikköön.</span><span class="sxs-lookup"><span data-stu-id="7b53b-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="7b53b-107">Kustannustoiminnan hierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="7b53b-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="7b53b-108">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="7b53b-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="7b53b-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-109">Click New.</span></span>
3. <span data-ttu-id="7b53b-110">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="7b53b-110">Click Create.</span></span>
4. <span data-ttu-id="7b53b-111">Kirjoita Dimensiohierarkian nimi -kenttään Kustannustoiminnan hierarkia.</span><span class="sxs-lookup"><span data-stu-id="7b53b-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="7b53b-112">Syötä tai valitse arvo Dimensio-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-113">Valitse Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="7b53b-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="7b53b-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7b53b-114">Click Save.</span></span>
7. <span data-ttu-id="7b53b-115">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="7b53b-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="7b53b-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-116">Click New.</span></span>
9. <span data-ttu-id="7b53b-117">Kirjoita arvo Solmun nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="7b53b-118">Syötä Kiinteä kustannus.</span><span class="sxs-lookup"><span data-stu-id="7b53b-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="7b53b-119">Valitse puussa Cost behavior hierarchy.</span><span class="sxs-lookup"><span data-stu-id="7b53b-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="7b53b-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-120">Click New.</span></span>
12. <span data-ttu-id="7b53b-121">Kirjoita arvo Solmun nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="7b53b-122">Syötä Muuttuva kustannus.</span><span class="sxs-lookup"><span data-stu-id="7b53b-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="7b53b-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7b53b-123">Click Save.</span></span>
14. <span data-ttu-id="7b53b-124">Valitse puussa Cost behavior hierarchy\Fixed cost.</span><span class="sxs-lookup"><span data-stu-id="7b53b-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="7b53b-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-125">Click New.</span></span>
16. <span data-ttu-id="7b53b-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7b53b-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="7b53b-127">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-128">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="7b53b-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="7b53b-129">Syötä tai valitse arvo Kohdedimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-130">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="7b53b-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="7b53b-131">Valitse puussa Cost behavior hierarchy\Variable cost.</span><span class="sxs-lookup"><span data-stu-id="7b53b-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="7b53b-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-132">Click New.</span></span>
21. <span data-ttu-id="7b53b-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7b53b-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="7b53b-134">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-135">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="7b53b-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="7b53b-136">Syötä tai valitse arvo Kohdedimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-137">Dimension jäsenten alue voi sisältää aukkoja, mutta jäsenet eivät voi olla päällekkäisiä.</span><span class="sxs-lookup"><span data-stu-id="7b53b-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="7b53b-138">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7b53b-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="7b53b-139">Käytännön ja sääntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="7b53b-139">Create the policy and rules</span></span>
1. <span data-ttu-id="7b53b-140">Valitse Kustannuslaskenta > Käytännöt > Kustannustoiminnan käytännöt.</span><span class="sxs-lookup"><span data-stu-id="7b53b-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="7b53b-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-141">Click New.</span></span>
3. <span data-ttu-id="7b53b-142">Kirjoita arvo Käytännön nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="7b53b-143">Syötä tai valitse arvo Kustannustason dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-144">Valitse äsken luotu käytäntöhierarkia.</span><span class="sxs-lookup"><span data-stu-id="7b53b-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="7b53b-145">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkia -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-146">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="7b53b-146">Select Organization.</span></span>  
6. <span data-ttu-id="7b53b-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7b53b-147">Click Save.</span></span>
7. <span data-ttu-id="7b53b-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-148">Click New.</span></span>
8. <span data-ttu-id="7b53b-149">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7b53b-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7b53b-150">Syötä tai valitse arvo Kustannustason dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-151">Laajenna hierarkia ja valitse Muuttuva kustannus.</span><span class="sxs-lookup"><span data-stu-id="7b53b-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="7b53b-152">Syötä tai valitse arvo Kustannusobjektin dimensiohierarkiasolmu -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="7b53b-153">Oletusarvoisesti muuttuva prosenttiosuus on 100.</span><span class="sxs-lookup"><span data-stu-id="7b53b-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="7b53b-154">Valitse Kustannusseurantayksikön käytännön määritykset.</span><span class="sxs-lookup"><span data-stu-id="7b53b-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="7b53b-155">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7b53b-155">Click New.</span></span>
13. <span data-ttu-id="7b53b-156">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7b53b-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="7b53b-157">Syötä päivämäärä Voimassa kirjanpitopäivästä alkaen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="7b53b-158">Säännöillä on voimaantulopäivämäärä. Käyttäjä tai järjestelmä voi määrittää säännön vanhentuneeksi, jos säännöstä luodaan uusi versio.</span><span class="sxs-lookup"><span data-stu-id="7b53b-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="7b53b-159">Anna tai valitse arvo Kustannusseurantayksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7b53b-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="7b53b-160">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7b53b-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]