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
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427075"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="f40e9-103">Tuotteiden luokitteluhierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="f40e9-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f40e9-104">Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f40e9-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="f40e9-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="f40e9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f40e9-106">Tämä menettely on tarkoitettu luokkapäällikölle.</span><span class="sxs-lookup"><span data-stu-id="f40e9-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="f40e9-107">Luo uusi luokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="f40e9-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="f40e9-108">Siirry kohtaan **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="f40e9-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-109">Click **New**.</span></span>
3. <span data-ttu-id="f40e9-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f40e9-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f40e9-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f40e9-112">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="f40e9-113">Luo hierarkia</span><span class="sxs-lookup"><span data-stu-id="f40e9-113">Build the hierarchy</span></span>
1. <span data-ttu-id="f40e9-114">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-114">Click **New** category node.</span></span>
2. <span data-ttu-id="f40e9-115">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f40e9-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="f40e9-116">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="f40e9-117">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="f40e9-118">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-118">Click **New** category node.</span></span>
6. <span data-ttu-id="f40e9-119">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f40e9-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="f40e9-120">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="f40e9-121">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="f40e9-122">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-122">Click **New** category node.</span></span>
10. <span data-ttu-id="f40e9-123">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f40e9-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="f40e9-124">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="f40e9-125">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="f40e9-126">Valitse **Uusi** luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-126">Click **New** category node.</span></span>
14. <span data-ttu-id="f40e9-127">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f40e9-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="f40e9-128">Kirjoita **Koodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="f40e9-129">Kirjoita **Kutsumanimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f40e9-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="f40e9-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="f40e9-131">Luokittele hierarkia</span><span class="sxs-lookup"><span data-stu-id="f40e9-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="f40e9-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f40e9-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f40e9-133">Valitse **toimintoruudussa** **Luokkahierarkia**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="f40e9-134">Valitse **Liitä hierarkiatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="f40e9-135">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-135">Click **New**.</span></span>
5. <span data-ttu-id="f40e9-136">Valitse **Luokkahierarkian tyyppi** -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f40e9-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="f40e9-137">Valitse **Tuoteluokituksen luokkahierarkian tyypin kauppatavarakoodi**.</span><span class="sxs-lookup"><span data-stu-id="f40e9-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="f40e9-138">Avaa haku napsauttamalla **Luokkahierarkia**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f40e9-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f40e9-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f40e9-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f40e9-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f40e9-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f40e9-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f40e9-141">Close the page.</span></span>

