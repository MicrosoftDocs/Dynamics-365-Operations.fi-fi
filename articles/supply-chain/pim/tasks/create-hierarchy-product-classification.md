---
title: Tuotteiden luokitteluhierarkian luominen
description: Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ff1a2ba20059d3fcb0347220e6e81130e03ac0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203730"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="1a6ef-103">Tuotteiden luokitteluhierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="1a6ef-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a6ef-104">Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="1a6ef-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1a6ef-106">Tämä menettely on tarkoitettu luokkapäällikölle.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="1a6ef-107">Luo uusi luokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="1a6ef-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="1a6ef-108">Siirry kohtaan **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="1a6ef-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-109">Click **New**.</span></span>
3. <span data-ttu-id="1a6ef-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="1a6ef-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1a6ef-112">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="1a6ef-113">Luo hierarkia</span><span class="sxs-lookup"><span data-stu-id="1a6ef-113">Build the hierarchy</span></span>
1. <span data-ttu-id="1a6ef-114">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-114">Click **New** category node.</span></span>
2. <span data-ttu-id="1a6ef-115">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="1a6ef-116">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="1a6ef-117">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="1a6ef-118">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-118">Click **New** category node.</span></span>
6. <span data-ttu-id="1a6ef-119">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="1a6ef-120">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="1a6ef-121">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="1a6ef-122">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-122">Click **New** category node.</span></span>
10. <span data-ttu-id="1a6ef-123">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="1a6ef-124">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="1a6ef-125">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="1a6ef-126">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-126">Click **New** category node.</span></span>
14. <span data-ttu-id="1a6ef-127">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="1a6ef-128">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="1a6ef-129">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="1a6ef-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="1a6ef-131">Luokittele hierarkia</span><span class="sxs-lookup"><span data-stu-id="1a6ef-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="1a6ef-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="1a6ef-133">Valitse **toimintoruudussa** **Luokkahierarkia**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="1a6ef-134">Valitse **Liitä hierarkiatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="1a6ef-135">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-135">Click **New**.</span></span>
5. <span data-ttu-id="1a6ef-136">Valitse **Luokkahierarkian tyyppi** -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="1a6ef-137">Valitse **Tuoteluokituksen luokkahierarkian tyypin kauppatavarakoodi**.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="1a6ef-138">Avaa haku napsauttamalla **Luokkahierarkia**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1a6ef-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1a6ef-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1a6ef-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1a6ef-141">Close the page.</span></span>

