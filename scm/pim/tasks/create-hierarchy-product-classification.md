--- 
title: Tuotteiden luokitteluhierarkian luominen
description: "Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="7d95d-103">Tuotteiden luokitteluhierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="7d95d-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d95d-104">Tässä menettelyssä selvitetään, miten uusi luokkahierarkia luodaan, ja määritetään kauppatavarahierarkian tyyppi.</span><span class="sxs-lookup"><span data-stu-id="7d95d-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="7d95d-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7d95d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7d95d-106">Tämä menettely on tarkoitettu luokkapäällikölle.</span><span class="sxs-lookup"><span data-stu-id="7d95d-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="7d95d-107">Luo uusi luokkahierarkia</span><span class="sxs-lookup"><span data-stu-id="7d95d-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="7d95d-108">Valitse Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat.</span><span class="sxs-lookup"><span data-stu-id="7d95d-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="7d95d-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d95d-109">Click New.</span></span>
3. <span data-ttu-id="7d95d-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7d95d-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d95d-112">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="7d95d-113">Luo hierarkia</span><span class="sxs-lookup"><span data-stu-id="7d95d-113">Build the hierarchy</span></span>
1. <span data-ttu-id="7d95d-114">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-114">Click New category node.</span></span>
2. <span data-ttu-id="7d95d-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="7d95d-116">Kirjoita Koodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="7d95d-117">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="7d95d-118">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-118">Click New category node.</span></span>
6. <span data-ttu-id="7d95d-119">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="7d95d-120">Kirjoita Koodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="7d95d-121">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="7d95d-122">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-122">Click New category node.</span></span>
10. <span data-ttu-id="7d95d-123">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="7d95d-124">Kirjoita Koodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="7d95d-125">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="7d95d-126">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-126">Click New category node.</span></span>
14. <span data-ttu-id="7d95d-127">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d95d-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="7d95d-128">Kirjoita Koodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="7d95d-129">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7d95d-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="7d95d-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="7d95d-131">Luokittele hierarkia</span><span class="sxs-lookup"><span data-stu-id="7d95d-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="7d95d-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7d95d-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="7d95d-133">Valitse toimintoruudussa Luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="7d95d-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="7d95d-134">Valitse Liitä hierarkiatyyppi.</span><span class="sxs-lookup"><span data-stu-id="7d95d-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="7d95d-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d95d-135">Click New.</span></span>
5. <span data-ttu-id="7d95d-136">Valitse Luokkahierarkian tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="7d95d-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="7d95d-137">Valitse tuoteluokituksen luokkahierarkian tyypin kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="7d95d-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="7d95d-138">Avaa haku napsauttamalla Luokkahierarkia-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="7d95d-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7d95d-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7d95d-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7d95d-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7d95d-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7d95d-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d95d-141">Close the page.</span></span>


