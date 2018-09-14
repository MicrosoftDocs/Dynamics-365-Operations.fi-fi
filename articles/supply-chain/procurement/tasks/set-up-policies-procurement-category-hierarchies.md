--- 
title: Aseta menettelytavat hankintaluokkien hierarkioille
description: "Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="6af7f-103">Aseta menettelytavat hankintaluokkien hierarkioille</span><span class="sxs-lookup"><span data-stu-id="6af7f-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6af7f-104">Tämän toiminnon avulla voit määrittää säännöt luokan tuotteiden tilaamista varten.</span><span class="sxs-lookup"><span data-stu-id="6af7f-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="6af7f-105">Käytäntösäännöt määritetään tietylle ostokäytännölle.</span><span class="sxs-lookup"><span data-stu-id="6af7f-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="6af7f-106">Luokan käyttöoikeuskäytäntösääntö ohjaa, mihin hankintaluokkiin työntekijöillä on käyttöoikeus luodessaan ehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="6af7f-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="6af7f-107">Ehdotusta luotaessa käytettävä ostokäytäntö ja luokan käyttöoikeussääntö määräytyvät perustuen yritykseen ja toimintayksikköön, johon työntekijä kuuluu.</span><span class="sxs-lookup"><span data-stu-id="6af7f-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="6af7f-108">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="6af7f-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="6af7f-109">Yleensä ostopäällikkö tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="6af7f-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="6af7f-110">Paikanna hankintakäytäntö</span><span class="sxs-lookup"><span data-stu-id="6af7f-110">Find the procurement policy</span></span>
1. <span data-ttu-id="6af7f-111">Siirry kohtaan Hankinnat > Asetukset > Käytännöt > Ostokäytännöt.</span><span class="sxs-lookup"><span data-stu-id="6af7f-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="6af7f-112">Napsauta hankintakäytännön USMF linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6af7f-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="6af7f-113">Tämä on käytäntö, johon sääntö lisätään.</span><span class="sxs-lookup"><span data-stu-id="6af7f-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="6af7f-114">Käytännön on oltava aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="6af7f-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="6af7f-115">Luokan käyttöoikeussäännön luominen</span><span class="sxs-lookup"><span data-stu-id="6af7f-115">Create a category access rule</span></span>
1. <span data-ttu-id="6af7f-116">Valitse luokan käyttöoikeuskäytäntöjen sääntö.</span><span class="sxs-lookup"><span data-stu-id="6af7f-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="6af7f-117">Jos Luo käytäntösääntö -painike näkyy himmennettynä, luokan käytössä on jo aktiivinen käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="6af7f-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="6af7f-118">Tarkista voimassaolo- ja erääntymispäiväkentistä mikä säännöistä on kyseessä, valitse se ja napsauta Keskeytä käytäntösääntö -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6af7f-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="6af7f-119">Mitään ei tarvitse tehdä, jos Luo käytäntösääntö -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6af7f-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="6af7f-120">Valitse Luo käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="6af7f-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="6af7f-121">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6af7f-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="6af7f-122">Aika ei saa olla päällekkäinen toisen, aktiivisen säännön kanssa.</span><span class="sxs-lookup"><span data-stu-id="6af7f-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="6af7f-123">Valitse luokka, jota sääntö koskee.</span><span class="sxs-lookup"><span data-stu-id="6af7f-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="6af7f-124">Kirjaa luokka muistiin – sitä tarvitaan myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="6af7f-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="6af7f-125">Kun valitset jonkin luokan, myös sen pääluokka tai -luokat lisätään myös Valitut luokat -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6af7f-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="6af7f-126">Valitse Sisällytä aliluokat -asetus, jos haluat käyttää sääntöä kaikkiin valitun luokan alaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="6af7f-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="6af7f-127">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="6af7f-127">Click Add.</span></span>
    * <span data-ttu-id="6af7f-128">Jos asetat Sisällytä yläluokka -vaihtoehdon käyttöön, pääluokalle määrittämäsi käytäntösääntö määritetään myös tämän alaluokille, jos alaluokille ei ole määritetty käytäntösääntöä.</span><span class="sxs-lookup"><span data-stu-id="6af7f-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="6af7f-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6af7f-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="6af7f-130">Luokan käytäntösäännön luominen</span><span class="sxs-lookup"><span data-stu-id="6af7f-130">Create a category policy rule</span></span>
1. <span data-ttu-id="6af7f-131">Valitse luokan käytäntösääntö</span><span class="sxs-lookup"><span data-stu-id="6af7f-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="6af7f-132">Jos Luo käytäntösääntö -painike on himmennettynä, valitse aktiivinen käytäntösääntö ja napsauta Keskeytä käytäntösääntö -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6af7f-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="6af7f-133">Valitse Luo käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="6af7f-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="6af7f-134">Syötä päivämäärä ja kellonaika Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6af7f-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="6af7f-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="6af7f-135">Click Add.</span></span>
5. <span data-ttu-id="6af7f-136">Valitse sama luokka, jota käytit luokan käyttöoikeussäännölle.</span><span class="sxs-lookup"><span data-stu-id="6af7f-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="6af7f-137">Valitse vaihtoehto Toimittajan valinta -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6af7f-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="6af7f-138">Valitse sääntö, joka ohjaa luokan toimittajavalintaa, kun ostoehdotuksia luodaan.</span><span class="sxs-lookup"><span data-stu-id="6af7f-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="6af7f-139">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="6af7f-139">Click Close.</span></span>
    * <span data-ttu-id="6af7f-140">Määrittämäsi käytäntösäännöt ovat olleet kulutustyypin ostoehdotuksille.</span><span class="sxs-lookup"><span data-stu-id="6af7f-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="6af7f-141">Jos haluat määrittää täydennystyypin ostoehdotusten käytäntöjä, luo sääntö käytäntösäännön tyypille "Täydennysluokan käyttöoikeuskäytäntöjen sääntö".</span><span class="sxs-lookup"><span data-stu-id="6af7f-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


