---
title: Käyttöomaisuuden kirjausprofiilien määrittäminen
description: Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "351099"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="20e38-103">Käyttöomaisuuden kirjausprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="20e38-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20e38-104">Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="20e38-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="20e38-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="20e38-106">Tehtävän ohjauksen esimerkeissä käsitellään peruskirjausprofiileja. Kirjausprofiileja on luotava myös erityisiä tilikartan ja taloushallinnon raportoinnin tarpeita varten.</span><span class="sxs-lookup"><span data-stu-id="20e38-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="20e38-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden kirjausprofiilit.</span><span class="sxs-lookup"><span data-stu-id="20e38-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="20e38-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="20e38-108">Click New.</span></span>
3. <span data-ttu-id="20e38-109">Kirjoita arvo Kirjausprofiili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20e38-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="20e38-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20e38-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="20e38-111">Jokaiselle käyttöomaisuuserien käsittelyssä käytettävälle käyttöomaisuuden tapahtumalajille on luotava kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="20e38-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="20e38-112">Tämä tehtävä ohjaus alkaa hankintatapahtumalajin käsittelyllä.</span><span class="sxs-lookup"><span data-stu-id="20e38-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="20e38-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-113">Click Add.</span></span>
6. <span data-ttu-id="20e38-114">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="20e38-115">Ryhmittelyt-kentän avulla voit määrittää taulun (määritetään yksi tili jokaiselle käyttöomaisuuserälle) tai ryhmän (määritetään yksi tili jokaiselle käyttöomaisuusryhmälle) kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="20e38-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="20e38-116">Tässä tehtäväoppaassa arvojoukoksi jätetään Kaikki, jolloin kaikissa käyttöomaisuuserissä käytetään määritettyä kirjaa.</span><span class="sxs-lookup"><span data-stu-id="20e38-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="20e38-117">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="20e38-118">Hankinnoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="20e38-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="20e38-119">Valitse Tapahtumalaji-kentässä Hankintaoikaisu.</span><span class="sxs-lookup"><span data-stu-id="20e38-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="20e38-120">Hankinnan oikaisutapahtumissa käytetään samoja tilejä kuin hankintatapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="20e38-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="20e38-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-121">Click Add.</span></span>
10. <span data-ttu-id="20e38-122">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="20e38-123">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="20e38-124">Hankintaoikaisuille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="20e38-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="20e38-125">Valitse Tapahtumalaji-kentässä Poisto.</span><span class="sxs-lookup"><span data-stu-id="20e38-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="20e38-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-126">Click Add.</span></span>
14. <span data-ttu-id="20e38-127">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="20e38-128">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="20e38-129">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="20e38-130">Valitse Tapahtumalaji-kentässä Poiston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="20e38-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="20e38-131">Poiston oikaisutapahtumissa käytetään samoja tilejä kuin poistotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="20e38-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="20e38-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-132">Click Add.</span></span>
19. <span data-ttu-id="20e38-133">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="20e38-134">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="20e38-135">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="20e38-136">Valitse Tapahtumalaji-kentässä Poisto - myynti.</span><span class="sxs-lookup"><span data-stu-id="20e38-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="20e38-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-137">Click Add.</span></span>
24. <span data-ttu-id="20e38-138">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="20e38-139">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="20e38-140">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="20e38-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="20e38-141">Valitse Tapahtumalaji-kentässä Poisto - hävikki.</span><span class="sxs-lookup"><span data-stu-id="20e38-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="20e38-142">Poistomyynnissä ja -hävikissä käytetään samoja tilejä.</span><span class="sxs-lookup"><span data-stu-id="20e38-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="20e38-143">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-143">Click Add.</span></span>
28. <span data-ttu-id="20e38-144">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="20e38-145">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="20e38-146">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="20e38-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="20e38-147">Laajenna Luovutus-osa.</span><span class="sxs-lookup"><span data-stu-id="20e38-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="20e38-148">Määritä poiston kirjausprofiilit sekä myynnille että hävikille.</span><span class="sxs-lookup"><span data-stu-id="20e38-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="20e38-149">Aloitetaan poistomyyntitapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="20e38-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="20e38-150">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-150">Click Add.</span></span>
32. <span data-ttu-id="20e38-151">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="20e38-152">Valitse Kirjausarvo-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="20e38-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="20e38-153">Hankinta-arvo koskee kaikkien vuosien hankinta-arvoja ja hankinnan oikaisun arvoja.</span><span class="sxs-lookup"><span data-stu-id="20e38-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="20e38-154">Voit myös määrittää tilit erikseen näille tapahtumalajeille.</span><span class="sxs-lookup"><span data-stu-id="20e38-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="20e38-155">Voit määrittää poistoprosessin käyttämään eri tilejä sen mukaan, onko poiston tuloksena voitto vai tappio.</span><span class="sxs-lookup"><span data-stu-id="20e38-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="20e38-156">Määritetään myynnin arvon tyypiksi Kaikki. Tällöin samoja tilejä käytetään kaikissa poistotyypeissä.</span><span class="sxs-lookup"><span data-stu-id="20e38-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="20e38-157">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="20e38-158">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="20e38-159">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-159">Click Add.</span></span>
37. <span data-ttu-id="20e38-160">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="20e38-161">Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="20e38-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="20e38-162">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="20e38-163">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="20e38-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-164">Click Add.</span></span>
41. <span data-ttu-id="20e38-165">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="20e38-166">Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="20e38-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="20e38-167">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="20e38-168">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="20e38-169">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-169">Click Add.</span></span>
46. <span data-ttu-id="20e38-170">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="20e38-171">Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="20e38-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="20e38-172">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="20e38-173">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="20e38-174">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-174">Click Add.</span></span>
51. <span data-ttu-id="20e38-175">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="20e38-176">Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="20e38-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="20e38-177">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="20e38-178">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="20e38-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-179">Click Add.</span></span>
56. <span data-ttu-id="20e38-180">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="20e38-181">Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="20e38-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="20e38-182">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="20e38-183">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="20e38-184">Valitse Myynti tai hävikki -kentässä Hävikki.</span><span class="sxs-lookup"><span data-stu-id="20e38-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="20e38-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-185">Click Add.</span></span>
62. <span data-ttu-id="20e38-186">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="20e38-187">Valitse Kirjausarvo-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="20e38-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="20e38-188">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="20e38-189">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="20e38-190">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-190">Click Add.</span></span>
67. <span data-ttu-id="20e38-191">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="20e38-192">Valitse Kirjausarvo-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="20e38-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="20e38-193">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="20e38-194">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="20e38-195">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-195">Click Add.</span></span>
71. <span data-ttu-id="20e38-196">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="20e38-197">Valitse Kirjausarvo-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="20e38-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="20e38-198">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="20e38-199">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="20e38-200">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-200">Click Add.</span></span>
76. <span data-ttu-id="20e38-201">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="20e38-202">Valitse Kirjausarvo-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="20e38-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="20e38-203">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="20e38-204">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="20e38-205">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-205">Click Add.</span></span>
81. <span data-ttu-id="20e38-206">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="20e38-207">Valitse Kirjausarvo-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="20e38-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="20e38-208">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="20e38-209">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="20e38-210">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="20e38-210">Click Add.</span></span>
86. <span data-ttu-id="20e38-211">Syötä tai valitse arvo kentässä Kirja.</span><span class="sxs-lookup"><span data-stu-id="20e38-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="20e38-212">Valitse Kirjausarvo-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="20e38-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="20e38-213">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="20e38-214">Määritä Vastatili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="20e38-214">In the Offset account field, specify the desired values.</span></span>

