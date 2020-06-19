---
title: Luo suljettu kysymys
description: Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428613"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="ad5fe-103">Luo suljettu kysymys</span><span class="sxs-lookup"><span data-stu-id="ad5fe-103">Create a closed ended question</span></span>



<span data-ttu-id="ad5fe-104">Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="ad5fe-105">Ensin luodaan vastaukset sisältävä vastausryhmä. Tämän jälkeen luodaan kysymys, joka käyttää vastausryhmää.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="ad5fe-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="ad5fe-107">Vastausryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="ad5fe-107">Create an answer group</span></span>
1. <span data-ttu-id="ad5fe-108">Valitse Kyselylomake > Suunnittelu > Vastausryhmät.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="ad5fe-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-109">Click New.</span></span>
3. <span data-ttu-id="ad5fe-110">Syötä Vastausryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="ad5fe-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ad5fe-112">Sijoita vastaukset satunnaiseen järjestykseen Muodosta satunnaisesti -toiminnon avulla aina, kun vastausryhmää käytetään kysymyksessä.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="ad5fe-113">Valitse Vastaus.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-113">Click Answer.</span></span>
6. <span data-ttu-id="ad5fe-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-114">Click New.</span></span>
    * <span data-ttu-id="ad5fe-115">Järjestysnumero määrittää vastausten näyttöjärjestyksen, ellei vastausryhmän Muodosta satunnaisesti -kohtaa ole valittu.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="ad5fe-116">Vastauksille voidaan myöntää pisteitä, kun kyselylomake pistetytetään.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="ad5fe-117">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="ad5fe-118">Oikea vastaus voidaan merkitä.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="ad5fe-119">Näin kyselylomakkeen pisteytyksessä usein tehdään.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="ad5fe-120">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="ad5fe-121">Jatka vastausryhmän vastausten valinnan asetusten luomista.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="ad5fe-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-122">Click New.</span></span>
10. <span data-ttu-id="ad5fe-123">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="ad5fe-124">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="ad5fe-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-125">Click New.</span></span>
13. <span data-ttu-id="ad5fe-126">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="ad5fe-127">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="ad5fe-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-128">Click New.</span></span>
16. <span data-ttu-id="ad5fe-129">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="ad5fe-130">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="ad5fe-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-131">Click New.</span></span>
19. <span data-ttu-id="ad5fe-132">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="ad5fe-133">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="ad5fe-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-134">Close the page.</span></span>
22. <span data-ttu-id="ad5fe-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="ad5fe-136">Kysymyksen luominen</span><span class="sxs-lookup"><span data-stu-id="ad5fe-136">Create the question</span></span>
1. <span data-ttu-id="ad5fe-137">Siirry kohtaan Kyselylomake > Suunnittelu > Kysymykset.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="ad5fe-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-138">Click New.</span></span>
3. <span data-ttu-id="ad5fe-139">Ryhmittele liittyvät kysymykset yhteen Tyyppi-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="ad5fe-140">Voit käyttää monivalintakysymyksissä valintaruudun, vaihtoehtopainikkeen tai yhdistelmäruudun syöttötyyppejä.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="ad5fe-141">Valitse vaihtoehto Syötetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="ad5fe-142">Anna tai valitse arvo Vastausryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="ad5fe-143">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad5fe-143">In the Text field, type a value.</span></span>

