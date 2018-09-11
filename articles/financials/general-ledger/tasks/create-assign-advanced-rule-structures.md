--- 
title: "Luo ja määritä lisäsääntörakenteet"
description: "Tässä tehtäväopastuksessa käsitellään lisäsääntörakenteen luomista ja sen määrittämistä tilirakenteeseen."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a371e2bd08ee3f65658e015990d46a430267add2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="0ccf3-103">Luo ja määritä lisäsääntörakenteet</span><span class="sxs-lookup"><span data-stu-id="0ccf3-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ccf3-104">Tässä tehtäväopastuksessa käsitellään lisäsääntörakenteen luomista ja sen määrittämistä tilirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="0ccf3-105">Opastuksessa käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="0ccf3-106">Luo kehittynyt sääntörakenne</span><span class="sxs-lookup"><span data-stu-id="0ccf3-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="0ccf3-107">Valitse Kirjanpito > Tilikartta > Rakenteet > Lisäsääntörakenteet.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="0ccf3-108">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="0ccf3-109">Kirjoita Lisäsääntörakenteet-kenttää sääntörakennetta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="0ccf3-110">Kirjoita Kuvaus-kenttään rakennetta kuvaava arvo.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="0ccf3-111">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-111">Click OK.</span></span>
6. <span data-ttu-id="0ccf3-112">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-112">Click Add segment.</span></span>
7. <span data-ttu-id="0ccf3-113">Valitse taloushallinnon dimensio segmenttiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="0ccf3-114">Esimerkki: myymälä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-114">For example, Store.</span></span>  
8. <span data-ttu-id="0ccf3-115">Valitse Lisää segmentti.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-115">Click Add segment.</span></span>
9. <span data-ttu-id="0ccf3-116">Avaa lisäsääntörakenne napsauttamalla luettelossa sen linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="0ccf3-117">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-117">Click Activate.</span></span>
11. <span data-ttu-id="0ccf3-118">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="0ccf3-119">Käytä lisäsääntörakennetta tilirakenteeseen</span><span class="sxs-lookup"><span data-stu-id="0ccf3-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="0ccf3-120">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-120">Close the form.</span></span>
2. <span data-ttu-id="0ccf3-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-121">Close the page.</span></span>
3. <span data-ttu-id="0ccf3-122">Valitse Kirjanpito > Tilikartta > Rakenteet > Määritä tilirakenteet.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="0ccf3-123">Etsi ja valitse luettelossa tilirakenne, johon haluat käyttää lisäsääntöä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="0ccf3-124">Avaa tilirakenne napsauttamalla sen nimeä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="0ccf3-125">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-125">Click Edit.</span></span>
    * <span data-ttu-id="0ccf3-126">Voit myös valita Lisäsäännöt, jolloin sinua pyydetään asettamalla tilirakenne luonnostilaan.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="0ccf3-127">Valitse Lisäsäännöt.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="0ccf3-128">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="0ccf3-129">Kirjoita arvo Lisäsääntö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="0ccf3-130">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="0ccf3-131">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-131">Click Create.</span></span>
12. <span data-ttu-id="0ccf3-132">Valitse Lisää uusia kriteerejä.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="0ccf3-133">Valitse Missä-kentässä päätili tai taloushallinnon dimensio.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="0ccf3-134">Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="0ccf3-135">Kirjoita arvo Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="0ccf3-136">Kirjoita kautta-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="0ccf3-137">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="0ccf3-138">Etsi luettelosta lisäsääntörakenne, jota haluat käyttää, kun antamasi ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="0ccf3-139">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-139">Click Add.</span></span>
20. <span data-ttu-id="0ccf3-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-140">Close the page.</span></span>
21. <span data-ttu-id="0ccf3-141">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-141">Click Activate.</span></span>
22. <span data-ttu-id="0ccf3-142">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="0ccf3-142">Click Activate.</span></span>


