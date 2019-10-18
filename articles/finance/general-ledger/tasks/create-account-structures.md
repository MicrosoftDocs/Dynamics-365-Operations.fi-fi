---
title: Tilirakenteiden luonti
description: Tässä opastuksessa käsitellään tilirakenteen luominen.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186253"
---
# <a name="create-account-structures"></a><span data-ttu-id="d25b6-103">Tilirakenteiden luonti</span><span class="sxs-lookup"><span data-stu-id="d25b6-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d25b6-104">Tässä opastuksessa käsitellään tilirakenteen luominen.</span><span class="sxs-lookup"><span data-stu-id="d25b6-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="d25b6-105">Vaiheissa käytetään esittely-tietojen USMF-yritystä.</span><span class="sxs-lookup"><span data-stu-id="d25b6-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="d25b6-106">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Tilirakenteiden konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="d25b6-107">Avaa pudotusvalikkoikkuna valitsemalla **toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="d25b6-108">Kirjoita **Tilirakenne**-kenttään nimi, joka kuvailee tilirakenteen tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="d25b6-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="d25b6-109">Kirjoita **Kuvaus**-kenttään kuvaus, joka määrittää tilirakenteen tarkoituksen.</span><span class="sxs-lookup"><span data-stu-id="d25b6-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="d25b6-110">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-110">Click **Create**.</span></span>
6. <span data-ttu-id="d25b6-111">Valitse **Segmentit ja sallitut arvot**-kohdasta **Lisää segmentti.**</span><span class="sxs-lookup"><span data-stu-id="d25b6-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="d25b6-112">Valitse dimensioluettelossa tilirakenteeseen lisättävä dimensio.</span><span class="sxs-lookup"><span data-stu-id="d25b6-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="d25b6-113">Valitse luettelon lopussa **Lisää segmentti**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="d25b6-114">Toista vaiheet 6-9 tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d25b6-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="d25b6-115">Voit muokata sallittuja arvoja valitsemalla segmentin **Sallitun arvon tiedot** -osassa.</span><span class="sxs-lookup"><span data-stu-id="d25b6-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="d25b6-116">Napsauta esimerkiksi **Päätili**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="d25b6-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="d25b6-117">Valitse **Käyttäjä**-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="d25b6-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="d25b6-118">Kirjoita arvo **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d25b6-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="d25b6-119">Esimerkki: 600000.</span><span class="sxs-lookup"><span data-stu-id="d25b6-119">For example, 600000.</span></span>  
13. <span data-ttu-id="d25b6-120">Kirjoita **kautta**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-120">In the **through** field, type a value.</span></span> <span data-ttu-id="d25b6-121">Esimerkki: 699999.</span><span class="sxs-lookup"><span data-stu-id="d25b6-121">For example, 699999.</span></span>  
14. <span data-ttu-id="d25b6-122">Valitse **Sallitun arvon tiedot** -osassa **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="d25b6-123">Toista vaiheet 10-15 tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d25b6-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="d25b6-124">Valitse **Sallitun arvon tiedot** -osassa **Lisää uusia kriteerejä**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="d25b6-125">Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="d25b6-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="d25b6-126">Kirjoita arvo **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d25b6-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="d25b6-127">Esimerkki: 033.</span><span class="sxs-lookup"><span data-stu-id="d25b6-127">For example, 033.</span></span>  
19. <span data-ttu-id="d25b6-128">Kirjoita **kautta**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-128">In the **through** field, type a value.</span></span> <span data-ttu-id="d25b6-129">Esimerkki: 034.</span><span class="sxs-lookup"><span data-stu-id="d25b6-129">For example, 034.</span></span>  
20. <span data-ttu-id="d25b6-130">Valitse **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-130">Click **Apply**.</span></span>
21. <span data-ttu-id="d25b6-131">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="d25b6-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="d25b6-132">Esimerkki: Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="d25b6-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="d25b6-133">Kirjoita **CostCenter**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="d25b6-134">Esimerkki: 007..021.</span><span class="sxs-lookup"><span data-stu-id="d25b6-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="d25b6-135">Valitse **Segmentit ja sallitut arvot**-kohdasta **Lisää.**</span><span class="sxs-lookup"><span data-stu-id="d25b6-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="d25b6-136">Kirjoita **MainAccount**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="d25b6-137">Esimerkki: 600000..699999</span><span class="sxs-lookup"><span data-stu-id="d25b6-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="d25b6-138">Voit muokata sallittuja arvoja valitsemalla ruudukossa segmentin.</span><span class="sxs-lookup"><span data-stu-id="d25b6-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="d25b6-139">Esimerkki: Osasto.</span><span class="sxs-lookup"><span data-stu-id="d25b6-139">For example, Department.</span></span>  
26. <span data-ttu-id="d25b6-140">Kirjoita Osasto-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-140">In the Department field, type a value.</span></span> <span data-ttu-id="d25b6-141">Esimerkki: 032.</span><span class="sxs-lookup"><span data-stu-id="d25b6-141">For example, 032.</span></span>  
27. <span data-ttu-id="d25b6-142">Kirjoita CostCenter-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d25b6-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="d25b6-143">Esimerkki: 086.</span><span class="sxs-lookup"><span data-stu-id="d25b6-143">For example, 086.</span></span>  
28. <span data-ttu-id="d25b6-144">Valitse **toimintoruudussa** **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="d25b6-145">Valitse **toimintoruudussa** **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="d25b6-146">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="d25b6-146">Click **Activate**.</span></span>
