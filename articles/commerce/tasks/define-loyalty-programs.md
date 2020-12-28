---
title: Määritä kanta-asiakasohjelmat
description: Seuraavassa kerrotaan, miten kaksi tasoa sisältävä kanta-asiakasohjelma määritetään.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f30d4d1b66e5b4b90f7df67d8f76a95a100338
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412015"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="2afd8-103">Määritä kanta-asiakasohjelmat</span><span class="sxs-lookup"><span data-stu-id="2afd8-103">Define loyalty programs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2afd8-104">Seuraavassa kerrotaan, miten kaksi tasoa sisältävä kanta-asiakasohjelma määritetään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="2afd8-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2afd8-106">Valitse Retail ja Commerce > ..</span><span class="sxs-lookup"><span data-stu-id="2afd8-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="2afd8-107">> Kanta-asiakasohjelmat.</span><span class="sxs-lookup"><span data-stu-id="2afd8-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="2afd8-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2afd8-108">Click New.</span></span>
3. <span data-ttu-id="2afd8-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2afd8-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2afd8-111">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="2afd8-111">Click Add line.</span></span>
6. <span data-ttu-id="2afd8-112">Syötä numero Taso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="2afd8-113">Syötä Taso-kenttään kanta-asiakkuustaso.</span><span class="sxs-lookup"><span data-stu-id="2afd8-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="2afd8-114">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2afd8-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2afd8-115">Avaa haku valitsemalla Päivämääräväli-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2afd8-116">Tämän päivämäärävälin tulee jatkua tulevaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="2afd8-116">This date interval should extend into the future.</span></span> <span data-ttu-id="2afd8-117">Jos kultatasolle on valittu päivämääräväliksi yhden vuoden jakso, jokainen asiakas, joka pätevöityy kultatasolle voi vastaanottaa yhden vuoden ajan kultatasolle määritettäviä palkkioita.</span><span class="sxs-lookup"><span data-stu-id="2afd8-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="2afd8-118">Jos asiakas saavuttaa uudelleen kultatason, kun hän on kyseisellä tasolla, päivämäärää, jona hänen tasonsa vanhenee, lykätään vuodella eteenpäin siitä päivästä, jona asiakas saavuttaa tason uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2afd8-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="2afd8-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2afd8-120">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="2afd8-120">Click Add line.</span></span>
12. <span data-ttu-id="2afd8-121">Syötä numero Taso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="2afd8-122">Syötä Taso-kenttään kanta-asiakkuustaso.</span><span class="sxs-lookup"><span data-stu-id="2afd8-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="2afd8-123">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2afd8-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="2afd8-124">Avaa haku valitsemalla Päivämääräväli-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="2afd8-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2afd8-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2afd8-126">Click Save.</span></span>
18. <span data-ttu-id="2afd8-127">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2afd8-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2afd8-128">Tasosäännöt määrittävät niiden palkkiopisteiden vähimmäismäärän, jotka tiettynä ajanjaksona on ansaittava ollakseen oikeutettu tasoon.</span><span class="sxs-lookup"><span data-stu-id="2afd8-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="2afd8-129">Ota käyttöön Tasosäännöt-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="2afd8-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="2afd8-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2afd8-130">Click New.</span></span>
    * <span data-ttu-id="2afd8-131">Yksi taso voi sisältää useita tasosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="2afd8-132">Tason ansaitsemiselle on voitu määrittää esimerkiksi kolme ehtoa, jotka ovat 500 euron suuruiset ostot kuukauden aikana, 1 000 euron suuruiset ostot vuoden aikana ja 20 tapahtuman tekeminen vuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="2afd8-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="2afd8-133">Tätä varten on luotava kolme tasosääntöä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="2afd8-134">Avaa haku valitsemalla Palkkiopiste-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2afd8-135">Tämän on oltava ei-lunastettava kanta-asiakasohjelman palkkiopiste.</span><span class="sxs-lookup"><span data-stu-id="2afd8-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="2afd8-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="2afd8-137">Syötä Myönnetyt pisteet vähintään -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2afd8-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="2afd8-138">Jos haluat asiakkaiden olevat oikeutettuja alimmalle tasolle yksinkertaisesti osallistumalla ohjelmaan, syötä 0.</span><span class="sxs-lookup"><span data-stu-id="2afd8-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="2afd8-139">Avaa haku valitsemalla Arviointipäivän aikaväli -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2afd8-140">Tämän päivämäärävälin tulee jatkua menneisyyteen.</span><span class="sxs-lookup"><span data-stu-id="2afd8-140">This date interval should extend into the past.</span></span> <span data-ttu-id="2afd8-141">Vain tämän päivämäärävälin aikana ansaitut pisteet lasketaan mukaan, kun tavoitellaan myönnettyjen vähimmäispisteiden arvoa.</span><span class="sxs-lookup"><span data-stu-id="2afd8-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="2afd8-142">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="2afd8-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2afd8-143">Click Save.</span></span>
27. <span data-ttu-id="2afd8-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2afd8-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="2afd8-145">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2afd8-145">Click New.</span></span>
29. <span data-ttu-id="2afd8-146">Avaa haku valitsemalla Palkkiopiste-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="2afd8-147">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="2afd8-148">Syötä Myönnetyt pisteet vähintään -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2afd8-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="2afd8-149">Avaa haku valitsemalla Arviointipäivän aikaväli -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2afd8-150">Tämän päivämäärävälin tulee jatkua menneisyyteen.</span><span class="sxs-lookup"><span data-stu-id="2afd8-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="2afd8-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="2afd8-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2afd8-152">Click Save.</span></span>
35. <span data-ttu-id="2afd8-153">Valitse Hintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="2afd8-153">Click Price groups.</span></span>
    * <span data-ttu-id="2afd8-154">Jos haluat antaa kanta-asiakkaille alennuksia,</span><span class="sxs-lookup"><span data-stu-id="2afd8-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="2afd8-155">määritä kanta-asiakasohjelmaan vähintään yksi hintaryhmä ja liitä hintaryhmä(t) alennuksiin.</span><span class="sxs-lookup"><span data-stu-id="2afd8-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="2afd8-156">Hintaryhmiä ja erityyppisiä alennusentiteettejä ei kannata yhdistää keskenään.</span><span class="sxs-lookup"><span data-stu-id="2afd8-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="2afd8-157">Älä käytä esimerkiksi samaa hintaryhmää kanta-asiakas- ja kanava-alennuksessa.</span><span class="sxs-lookup"><span data-stu-id="2afd8-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="2afd8-158">Avaa haku valitsemalla Hintaryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2afd8-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2afd8-159">Sivun yläosassa oleva Hintaryhmät-linkki koskee kanta-asiakasohjelmaa.</span><span class="sxs-lookup"><span data-stu-id="2afd8-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="2afd8-160">Ohjelman tasot -pikavälilehden Hintaryhmät-linkki koskee vain tiettyä kanta-asiakkuustasoa.</span><span class="sxs-lookup"><span data-stu-id="2afd8-160">The Price groups link in the Program tiers FastTab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="2afd8-161">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2afd8-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="2afd8-162">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2afd8-162">Click Save.</span></span>
39. <span data-ttu-id="2afd8-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2afd8-163">Close the page.</span></span>
40. <span data-ttu-id="2afd8-164">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2afd8-164">Click Save.</span></span>

