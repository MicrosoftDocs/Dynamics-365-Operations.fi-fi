--- 
title: Luo suljettu kysymys
description: Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fdfac92b80774adb8376d5c2e945d063173188c8
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="97aaa-103">Luo suljettu kysymys</span><span class="sxs-lookup"><span data-stu-id="97aaa-103">Create a closed ended question</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97aaa-104">Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.</span><span class="sxs-lookup"><span data-stu-id="97aaa-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="97aaa-105">Ensin luodaan vastaukset sisältävä vastausryhmä. Tämän jälkeen luodaan kysymys, joka käyttää vastausryhmää.</span><span class="sxs-lookup"><span data-stu-id="97aaa-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="97aaa-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="97aaa-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="97aaa-107">Vastausryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="97aaa-107">Create an answer group</span></span>
1. <span data-ttu-id="97aaa-108">Valitse Kyselylomake > Suunnittelu > Vastausryhmät.</span><span class="sxs-lookup"><span data-stu-id="97aaa-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="97aaa-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-109">Click New.</span></span>
3. <span data-ttu-id="97aaa-110">Syötä Vastausryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="97aaa-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aaa-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="97aaa-112">Sijoita vastaukset satunnaiseen järjestykseen Muodosta satunnaisesti -toiminnon avulla aina, kun vastausryhmää käytetään kysymyksessä.</span><span class="sxs-lookup"><span data-stu-id="97aaa-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="97aaa-113">Valitse Vastaus.</span><span class="sxs-lookup"><span data-stu-id="97aaa-113">Click Answer.</span></span>
6. <span data-ttu-id="97aaa-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-114">Click New.</span></span>
    * <span data-ttu-id="97aaa-115">Järjestysnumero määrittää vastausten näyttöjärjestyksen, ellei vastausryhmän Muodosta satunnaisesti -kohtaa ole valittu.</span><span class="sxs-lookup"><span data-stu-id="97aaa-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="97aaa-116">Vastauksille voidaan myöntää pisteitä, kun kyselylomake pistetytetään.</span><span class="sxs-lookup"><span data-stu-id="97aaa-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="97aaa-117">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="97aaa-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="97aaa-118">Oikea vastaus voidaan merkitä.</span><span class="sxs-lookup"><span data-stu-id="97aaa-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="97aaa-119">Näin kyselylomakkeen pisteytyksessä usein tehdään.</span><span class="sxs-lookup"><span data-stu-id="97aaa-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="97aaa-120">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="97aaa-121">Jatka vastausryhmän vastausten valinnan asetusten luomista.</span><span class="sxs-lookup"><span data-stu-id="97aaa-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="97aaa-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-122">Click New.</span></span>
10. <span data-ttu-id="97aaa-123">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="97aaa-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="97aaa-124">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="97aaa-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-125">Click New.</span></span>
13. <span data-ttu-id="97aaa-126">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="97aaa-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="97aaa-127">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="97aaa-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-128">Click New.</span></span>
16. <span data-ttu-id="97aaa-129">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="97aaa-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="97aaa-130">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="97aaa-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-131">Click New.</span></span>
19. <span data-ttu-id="97aaa-132">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="97aaa-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="97aaa-133">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="97aaa-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="97aaa-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="97aaa-134">Close the page.</span></span>
22. <span data-ttu-id="97aaa-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="97aaa-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="97aaa-136">Kysymyksen luominen</span><span class="sxs-lookup"><span data-stu-id="97aaa-136">Create the question</span></span>
1. <span data-ttu-id="97aaa-137">Siirry kohtaan Kyselylomake > Suunnittelu > Kysymykset.</span><span class="sxs-lookup"><span data-stu-id="97aaa-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="97aaa-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97aaa-138">Click New.</span></span>
3. <span data-ttu-id="97aaa-139">Ryhmittele liittyvät kysymykset yhteen Tyyppi-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="97aaa-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="97aaa-140">Voit käyttää monivalintakysymyksissä valintaruudun, vaihtoehtopainikkeen tai yhdistelmäruudun syöttötyyppejä.</span><span class="sxs-lookup"><span data-stu-id="97aaa-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="97aaa-141">Valitse vaihtoehto Syötetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="97aaa-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="97aaa-142">Anna tai valitse arvo Vastausryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aaa-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="97aaa-143">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97aaa-143">In the Text field, type a value.</span></span>


