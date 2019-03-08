---
title: Tilirakenteiden luonti
description: Tässä opastuksessa käsitellään tilirakenteen luominen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "356389"
---
# <a name="create-account-structures"></a><span data-ttu-id="cf30c-103">Tilirakenteiden luonti</span><span class="sxs-lookup"><span data-stu-id="cf30c-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf30c-104">Tässä opastuksessa käsitellään tilirakenteen luominen.</span><span class="sxs-lookup"><span data-stu-id="cf30c-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="cf30c-105">Vaiheissa käytetään esittely-tietojen USMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="cf30c-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="cf30c-106">Valitse Kirjanpito > Tilikartta > Rakenteet > Määritä tilirakenteet.</span><span class="sxs-lookup"><span data-stu-id="cf30c-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="cf30c-107">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="cf30c-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="cf30c-108">Kirjoita Tilirakenne-kenttään nimi, joka kuvailee tilirakenteen tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="cf30c-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="cf30c-109">Kirjoita Kuvaus-kenttään kuvaus, joka määrittää tilirakenteen tarkoituksen.</span><span class="sxs-lookup"><span data-stu-id="cf30c-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="cf30c-110">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-110">Click Create.</span></span>
6. <span data-ttu-id="cf30c-111">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-111">Click Add segment.</span></span>
7. <span data-ttu-id="cf30c-112">Valitse Dimensiot-luettelossa tilirakenteeseen lisättävä dimensio.</span><span class="sxs-lookup"><span data-stu-id="cf30c-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="cf30c-113">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-113">Click Add segment.</span></span>
9. <span data-ttu-id="cf30c-114">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-114">Click Add segment.</span></span>
10. <span data-ttu-id="cf30c-115">Valitse Dimensiot-luettelossa tilirakenteeseen lisättävä dimensio.</span><span class="sxs-lookup"><span data-stu-id="cf30c-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="cf30c-116">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-116">Click Add segment.</span></span>
12. <span data-ttu-id="cf30c-117">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-117">Click Add segment.</span></span>
13. <span data-ttu-id="cf30c-118">Valitse Dimensiot-luettelossa tilirakenteeseen lisättävä dimensio.</span><span class="sxs-lookup"><span data-stu-id="cf30c-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="cf30c-119">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="cf30c-119">Click Add segment.</span></span>
15. <span data-ttu-id="cf30c-120">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="cf30c-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cf30c-121">Napsauta esimerkiksi päätilissä.</span><span class="sxs-lookup"><span data-stu-id="cf30c-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="cf30c-122">Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="cf30c-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="cf30c-123">Kirjoita arvo Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf30c-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cf30c-124">Esimerkki: 600000.</span><span class="sxs-lookup"><span data-stu-id="cf30c-124">For example, 600000.</span></span>  
18. <span data-ttu-id="cf30c-125">Kirjoita kautta-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="cf30c-126">Esimerkki: 699999.</span><span class="sxs-lookup"><span data-stu-id="cf30c-126">For example, 699999.</span></span>  
19. <span data-ttu-id="cf30c-127">Valitse Apply.</span><span class="sxs-lookup"><span data-stu-id="cf30c-127">Click Apply.</span></span>
20. <span data-ttu-id="cf30c-128">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="cf30c-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cf30c-129">Esimerkki: Osasto.</span><span class="sxs-lookup"><span data-stu-id="cf30c-129">For example, Department.</span></span>  
21. <span data-ttu-id="cf30c-130">Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="cf30c-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="cf30c-131">Kirjoita arvo Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf30c-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cf30c-132">Esimerkki: 022.</span><span class="sxs-lookup"><span data-stu-id="cf30c-132">For example, 022.</span></span>  
23. <span data-ttu-id="cf30c-133">Kirjoita kautta-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="cf30c-134">Esimerkki: 031.</span><span class="sxs-lookup"><span data-stu-id="cf30c-134">For example, 031.</span></span>  
24. <span data-ttu-id="cf30c-135">Valitse Lisää uusia kriteerejä.</span><span class="sxs-lookup"><span data-stu-id="cf30c-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="cf30c-136">Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="cf30c-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="cf30c-137">Kirjoita arvo Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cf30c-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cf30c-138">Esimerkki: 033.</span><span class="sxs-lookup"><span data-stu-id="cf30c-138">For example, 033.</span></span>  
27. <span data-ttu-id="cf30c-139">Kirjoita kautta-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="cf30c-140">Esimerkki: 034.</span><span class="sxs-lookup"><span data-stu-id="cf30c-140">For example, 034.</span></span>  
28. <span data-ttu-id="cf30c-141">Valitse Apply.</span><span class="sxs-lookup"><span data-stu-id="cf30c-141">Click Apply.</span></span>
29. <span data-ttu-id="cf30c-142">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="cf30c-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cf30c-143">Esimerkki: Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="cf30c-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="cf30c-144">Kirjoita CostCenter-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="cf30c-145">Esimerkki: 007..021.</span><span class="sxs-lookup"><span data-stu-id="cf30c-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="cf30c-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="cf30c-146">Click Add.</span></span>
32. <span data-ttu-id="cf30c-147">Kirjoita MainAccount-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="cf30c-148">Esimerkki: 600000..699999</span><span class="sxs-lookup"><span data-stu-id="cf30c-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="cf30c-149">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="cf30c-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="cf30c-150">Esimerkki: Osasto.</span><span class="sxs-lookup"><span data-stu-id="cf30c-150">For example, Department.</span></span>  
34. <span data-ttu-id="cf30c-151">Kirjoita Osasto-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="cf30c-152">Esimerkki: 032.</span><span class="sxs-lookup"><span data-stu-id="cf30c-152">For example, 032.</span></span>  
35. <span data-ttu-id="cf30c-153">Kirjoita CostCenter-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cf30c-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="cf30c-154">Esimerkki: 086.</span><span class="sxs-lookup"><span data-stu-id="cf30c-154">For example, 086.</span></span>  
36. <span data-ttu-id="cf30c-155">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="cf30c-155">Click Validate.</span></span>
37. <span data-ttu-id="cf30c-156">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="cf30c-156">Click Activate.</span></span>
38. <span data-ttu-id="cf30c-157">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="cf30c-157">Click Activate.</span></span>

