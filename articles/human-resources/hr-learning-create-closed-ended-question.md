---
title: Luo suljettu kysymys
description: Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41e12e6f35237ea125756b502d5cebed58c6bf55
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790641"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="a1fec-103">Luo suljettu kysymys</span><span class="sxs-lookup"><span data-stu-id="a1fec-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="a1fec-104">Monivalintakysymysten avulla voit antaa vastaajille vastauksia, joista he voivat valita.</span><span class="sxs-lookup"><span data-stu-id="a1fec-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="a1fec-105">Ensin luodaan vastaukset sisältävä vastausryhmä. Tämän jälkeen luodaan kysymys, joka käyttää vastausryhmää.</span><span class="sxs-lookup"><span data-stu-id="a1fec-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="a1fec-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a1fec-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="a1fec-107">Vastausryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="a1fec-107">Create an answer group</span></span>
1. <span data-ttu-id="a1fec-108">Valitse Kyselylomake > Suunnittelu > Vastausryhmät.</span><span class="sxs-lookup"><span data-stu-id="a1fec-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="a1fec-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-109">Click New.</span></span>
3. <span data-ttu-id="a1fec-110">Syötä Vastausryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="a1fec-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a1fec-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a1fec-112">Sijoita vastaukset satunnaiseen järjestykseen Muodosta satunnaisesti -toiminnon avulla aina, kun vastausryhmää käytetään kysymyksessä.</span><span class="sxs-lookup"><span data-stu-id="a1fec-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="a1fec-113">Valitse Vastaus.</span><span class="sxs-lookup"><span data-stu-id="a1fec-113">Click Answer.</span></span>
6. <span data-ttu-id="a1fec-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-114">Click New.</span></span>
    * <span data-ttu-id="a1fec-115">Järjestysnumero määrittää vastausten näyttöjärjestyksen, ellei vastausryhmän Muodosta satunnaisesti -kohtaa ole valittu.</span><span class="sxs-lookup"><span data-stu-id="a1fec-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="a1fec-116">Vastauksille voidaan myöntää pisteitä, kun kyselylomake pistetytetään.</span><span class="sxs-lookup"><span data-stu-id="a1fec-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="a1fec-117">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a1fec-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="a1fec-118">Oikea vastaus voidaan merkitä.</span><span class="sxs-lookup"><span data-stu-id="a1fec-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="a1fec-119">Näin kyselylomakkeen pisteytyksessä usein tehdään.</span><span class="sxs-lookup"><span data-stu-id="a1fec-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="a1fec-120">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="a1fec-121">Jatka vastausryhmän vastausten valinnan asetusten luomista.</span><span class="sxs-lookup"><span data-stu-id="a1fec-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="a1fec-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-122">Click New.</span></span>
10. <span data-ttu-id="a1fec-123">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a1fec-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="a1fec-124">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="a1fec-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-125">Click New.</span></span>
13. <span data-ttu-id="a1fec-126">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a1fec-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="a1fec-127">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="a1fec-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-128">Click New.</span></span>
16. <span data-ttu-id="a1fec-129">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a1fec-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="a1fec-130">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="a1fec-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-131">Click New.</span></span>
19. <span data-ttu-id="a1fec-132">Syötä Pisteet-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a1fec-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="a1fec-133">Syötä Vastaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a1fec-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="a1fec-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a1fec-134">Close the page.</span></span>
22. <span data-ttu-id="a1fec-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a1fec-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="a1fec-136">Kysymyksen luominen</span><span class="sxs-lookup"><span data-stu-id="a1fec-136">Create the question</span></span>
1. <span data-ttu-id="a1fec-137">Siirry kohtaan Kyselylomake > Suunnittelu > Kysymykset.</span><span class="sxs-lookup"><span data-stu-id="a1fec-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="a1fec-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a1fec-138">Click New.</span></span>
3. <span data-ttu-id="a1fec-139">Ryhmittele liittyvät kysymykset yhteen Tyyppi-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="a1fec-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="a1fec-140">Voit käyttää monivalintakysymyksissä valintaruudun, vaihtoehtopainikkeen tai yhdistelmäruudun syöttötyyppejä.</span><span class="sxs-lookup"><span data-stu-id="a1fec-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="a1fec-141">Valitse vaihtoehto Syötetyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a1fec-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="a1fec-142">Anna tai valitse arvo Vastausryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a1fec-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="a1fec-143">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a1fec-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]