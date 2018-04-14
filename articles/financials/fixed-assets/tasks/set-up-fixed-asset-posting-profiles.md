--- 
title: "Käyttöomaisuuden kirjausprofiilien määrittäminen"
description: "Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9bd8a506fc0bbf4d4d8127afa71fe371be10b55b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="946be-103">Käyttöomaisuuden kirjausprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="946be-103">Set up fixed asset posting profiles</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="946be-104">Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.</span><span class="sxs-lookup"><span data-stu-id="946be-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="946be-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="946be-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="946be-106">Tehtävän ohjauksen esimerkeissä käsitellään peruskirjausprofiileja. Kirjausprofiileja on luotava myös erityisiä tilikartan ja taloushallinnon raportoinnin tarpeita varten.</span><span class="sxs-lookup"><span data-stu-id="946be-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="946be-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden kirjausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="946be-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="946be-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="946be-108">Click New.</span></span>
3. <span data-ttu-id="946be-109">Kirjoita arvo Kirjausprofiili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="946be-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="946be-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="946be-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="946be-111">Jokaiselle käyttöomaisuuserien käsittelyssä käytettävälle käyttöomaisuuden tapahtumalajille on luotava kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="946be-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="946be-112">Tämä tehtävä ohjaus alkaa hankintatapahtumalajin käsittelyllä.</span><span class="sxs-lookup"><span data-stu-id="946be-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="946be-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-113">Click Add.</span></span>
6. <span data-ttu-id="946be-114">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="946be-115">Ryhmittelyt-kentän avulla voit määrittää taulun (määritetään yksi tili jokaiselle käyttöomaisuuserälle) tai ryhmän (määritetään yksi tili jokaiselle käyttöomaisuusryhmälle) kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="946be-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="946be-116">Tässä tehtäväoppaassa arvojoukoksi jätetään Kaikki, jolloin kaikissa käyttöomaisuuserissä käytetään määritettyä kirjaa.</span><span class="sxs-lookup"><span data-stu-id="946be-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="946be-117">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="946be-118">Hankinnoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="946be-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="946be-119">Valitse Tapahtumalaji-kentässä Hankintaoikaisu.</span><span class="sxs-lookup"><span data-stu-id="946be-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="946be-120">Hankinnan oikaisutapahtumissa käytetään samoja tilejä kuin hankintatapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="946be-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="946be-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-121">Click Add.</span></span>
10. <span data-ttu-id="946be-122">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="946be-123">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="946be-124">Hankintaoikaisuille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="946be-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="946be-125">Valitse Tapahtumalaji-kentässä Poisto.</span><span class="sxs-lookup"><span data-stu-id="946be-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="946be-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-126">Click Add.</span></span>
14. <span data-ttu-id="946be-127">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="946be-128">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="946be-129">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="946be-130">Valitse Tapahtumalaji-kentässä Poiston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="946be-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="946be-131">Poiston oikaisutapahtumissa käytetään samoja tilejä kuin poistotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="946be-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="946be-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-132">Click Add.</span></span>
19. <span data-ttu-id="946be-133">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="946be-134">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="946be-135">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="946be-136">Valitse Tapahtumalaji-kentässä Poisto - myynti.</span><span class="sxs-lookup"><span data-stu-id="946be-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="946be-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-137">Click Add.</span></span>
24. <span data-ttu-id="946be-138">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="946be-139">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="946be-140">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="946be-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="946be-141">Valitse Tapahtumalaji-kentässä Poisto - hävikki.</span><span class="sxs-lookup"><span data-stu-id="946be-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="946be-142">Poistomyynnissä ja -hävikissä käytetään samoja tilejä.</span><span class="sxs-lookup"><span data-stu-id="946be-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="946be-143">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-143">Click Add.</span></span>
28. <span data-ttu-id="946be-144">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="946be-145">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="946be-146">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="946be-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="946be-147">Laajenna Luovutus-osa.</span><span class="sxs-lookup"><span data-stu-id="946be-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="946be-148">Määritä poiston kirjausprofiilit sekä myynnille että hävikille.</span><span class="sxs-lookup"><span data-stu-id="946be-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="946be-149">Aloitetaan poistomyyntitapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="946be-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="946be-150">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-150">Click Add.</span></span>
32. <span data-ttu-id="946be-151">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="946be-152">Valitse Kirjausarvo-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="946be-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="946be-153">Hankinta-arvo koskee kaikkien vuosien hankinta-arvoja ja hankinnan oikaisun arvoja.</span><span class="sxs-lookup"><span data-stu-id="946be-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="946be-154">Voit myös määrittää tilit erikseen näille tapahtumalajeille.</span><span class="sxs-lookup"><span data-stu-id="946be-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="946be-155">Voit määrittää poistoprosessin käyttämään eri tilejä sen mukaan, onko poiston tuloksena voitto vai tappio.</span><span class="sxs-lookup"><span data-stu-id="946be-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="946be-156">Määritetään myynnin arvon tyypiksi Kaikki. Tällöin samoja tilejä käytetään kaikissa poistotyypeissä.</span><span class="sxs-lookup"><span data-stu-id="946be-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="946be-157">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="946be-158">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="946be-159">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-159">Click Add.</span></span>
37. <span data-ttu-id="946be-160">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="946be-161">Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="946be-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="946be-162">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="946be-163">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="946be-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-164">Click Add.</span></span>
41. <span data-ttu-id="946be-165">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="946be-166">Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="946be-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="946be-167">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="946be-168">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="946be-169">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-169">Click Add.</span></span>
46. <span data-ttu-id="946be-170">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="946be-171">Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="946be-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="946be-172">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="946be-173">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="946be-174">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-174">Click Add.</span></span>
51. <span data-ttu-id="946be-175">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="946be-176">Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="946be-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="946be-177">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="946be-178">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="946be-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-179">Click Add.</span></span>
56. <span data-ttu-id="946be-180">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="946be-181">Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="946be-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="946be-182">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="946be-183">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="946be-184">Valitse Myynti tai hävikki -kentässä Hävikki.</span><span class="sxs-lookup"><span data-stu-id="946be-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="946be-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-185">Click Add.</span></span>
62. <span data-ttu-id="946be-186">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="946be-187">Valitse Kirjausarvo-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="946be-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="946be-188">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="946be-189">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="946be-190">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-190">Click Add.</span></span>
67. <span data-ttu-id="946be-191">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="946be-192">Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="946be-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="946be-193">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="946be-194">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="946be-195">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-195">Click Add.</span></span>
71. <span data-ttu-id="946be-196">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="946be-197">Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="946be-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="946be-198">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="946be-199">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="946be-200">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-200">Click Add.</span></span>
76. <span data-ttu-id="946be-201">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="946be-202">Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="946be-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="946be-203">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="946be-204">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="946be-205">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-205">Click Add.</span></span>
81. <span data-ttu-id="946be-206">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="946be-207">Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="946be-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="946be-208">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="946be-209">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="946be-210">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="946be-210">Click Add.</span></span>
86. <span data-ttu-id="946be-211">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="946be-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="946be-212">Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="946be-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="946be-213">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="946be-214">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="946be-214">In the Offset account field, specify the desired values.</span></span>


