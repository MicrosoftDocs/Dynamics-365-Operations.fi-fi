---
title: Luo suljettu kysymys
description: Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 65d77806498c3a710c00865ad27716f50796cdf5
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5114953"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="aa0f5-103">Luo suljettu kysymys</span><span class="sxs-lookup"><span data-stu-id="aa0f5-103">Create a closed ended question</span></span>



<span data-ttu-id="aa0f5-104">Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="aa0f5-105">Ensin luodaan vastaukset sisältävä vastausryhmä. Tämän jälkeen luodaan kysymys, joka käyttää vastausryhmää.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="aa0f5-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="aa0f5-107">Vastausryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="aa0f5-107">Create an answer group</span></span>
1. <span data-ttu-id="aa0f5-108">Valitse Kyselylomake > Suunnittelu > Vastausryhmät.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="aa0f5-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-109">Click New.</span></span>
3. <span data-ttu-id="aa0f5-110">Syötä Vastausryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="aa0f5-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="aa0f5-112">Sijoita vastaukset satunnaiseen järjestykseen Muodosta satunnaisesti -toiminnon avulla aina, kun vastausryhmää käytetään kysymyksessä.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="aa0f5-113">Valitse Vastaus.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-113">Click Answer.</span></span>
6. <span data-ttu-id="aa0f5-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-114">Click New.</span></span>
    * <span data-ttu-id="aa0f5-115">Järjestysnumero määrittää vastausten näyttöjärjestyksen, ellei vastausryhmän Muodosta satunnaisesti -kohtaa ole valittu.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="aa0f5-116">Vastauksille voidaan myöntää pisteitä, kun kyselylomake pistetytetään.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="aa0f5-117">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="aa0f5-118">Oikea vastaus voidaan merkitä.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="aa0f5-119">Näin kyselylomakkeen pisteytyksessä usein tehdään.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="aa0f5-120">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="aa0f5-121">Jatka vastausryhmän vastausten valinnan asetusten luomista.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="aa0f5-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-122">Click New.</span></span>
10. <span data-ttu-id="aa0f5-123">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="aa0f5-124">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="aa0f5-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-125">Click New.</span></span>
13. <span data-ttu-id="aa0f5-126">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="aa0f5-127">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="aa0f5-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-128">Click New.</span></span>
16. <span data-ttu-id="aa0f5-129">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="aa0f5-130">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="aa0f5-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-131">Click New.</span></span>
19. <span data-ttu-id="aa0f5-132">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="aa0f5-133">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="aa0f5-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-134">Close the page.</span></span>
22. <span data-ttu-id="aa0f5-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="aa0f5-136">Kysymyksen luominen</span><span class="sxs-lookup"><span data-stu-id="aa0f5-136">Create the question</span></span>
1. <span data-ttu-id="aa0f5-137">Siirry kohtaan Kyselylomake > Suunnittelu > Kysymykset.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="aa0f5-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-138">Click New.</span></span>
3. <span data-ttu-id="aa0f5-139">Ryhmittele liittyvät kysymykset yhteen Tyyppi-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="aa0f5-140">Voit käyttää monivalintakysymyksissä valintaruudun, vaihtoehtopainikkeen tai yhdistelmäruudun syöttötyyppejä.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="aa0f5-141">Valitse vaihtoehto Syötetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="aa0f5-142">Anna tai valitse arvo Vastausryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="aa0f5-143">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa0f5-143">In the Text field, type a value.</span></span>

