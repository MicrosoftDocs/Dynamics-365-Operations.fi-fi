---
title: Käyttöomaisuuden kirjausprofiilien määrittäminen
description: Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 494af854d408f0b0c02d753ff3d24eb3d6216fd9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177507"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="37a3d-103">Käyttöomaisuuden kirjausprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37a3d-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37a3d-104">Tässä tehtävän ohjauksessa määritetään käyttöomaisuuden kirjausarvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="37a3d-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="37a3d-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="37a3d-106">Tehtävän ohjauksen esimerkeissä käsitellään peruskirjausprofiileja. Kirjausprofiileja on luotava myös erityisiä tilikartan ja taloushallinnon raportoinnin tarpeita varten.</span><span class="sxs-lookup"><span data-stu-id="37a3d-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="37a3d-107">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Asetukset > Käyttöomaisuuserän kirjausprofiili**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-107">In the Navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset posting profiles**.</span></span>
2. <span data-ttu-id="37a3d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-108">Click **New**.</span></span>
3. <span data-ttu-id="37a3d-109">Kirjoita arvo **Kirjausprofiili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="37a3d-109">In the **Posting profile** field, type a value.</span></span>
4. <span data-ttu-id="37a3d-110">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="37a3d-110">In the **Description** field, type a value.</span></span> <span data-ttu-id="37a3d-111">Jokaiselle käyttöomaisuuserien käsittelyssä käytettävälle käyttöomaisuuden tapahtumalajille on luotava kirjausprofiili.</span><span class="sxs-lookup"><span data-stu-id="37a3d-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span> <span data-ttu-id="37a3d-112">Tämä tehtävä ohjaus alkaa hankintatapahtumalajin käsittelyllä.</span><span class="sxs-lookup"><span data-stu-id="37a3d-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="37a3d-113">Napsauta **Lisää** valikkorivillä.</span><span class="sxs-lookup"><span data-stu-id="37a3d-113">In the toolbar, click **Add**.</span></span>
6. <span data-ttu-id="37a3d-114">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-114">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="37a3d-115">**Ryhmittelyt**-kentän avulla voit määrittää taulun (määritetään yksi tili jokaiselle käyttöomaisuuserälle) tai ryhmän (määritetään yksi tili jokaiselle käyttöomaisuusryhmälle) kirjausprofiilin.</span><span class="sxs-lookup"><span data-stu-id="37a3d-115">The **Groupings** field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span> <span data-ttu-id="37a3d-116">Tässä tehtäväoppaassa arvojoukoksi jätetään Kaikki, jolloin kaikissa käyttöomaisuuserissä käytetään määritettyä kirjaa.</span><span class="sxs-lookup"><span data-stu-id="37a3d-116">For this task guide, leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="37a3d-117">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-117">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="37a3d-118">Hankinnoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="37a3d-118">For acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="37a3d-119">Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Hankintaoikaisu.</span><span class="sxs-lookup"><span data-stu-id="37a3d-119">In the drop-down menu under the **Ledger accounts** fastTab, select 'Acquisition adjustment'.</span></span> <span data-ttu-id="37a3d-120">Hankinnan oikaisutapahtumissa käytetään samoja tilejä kuin hankintatapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="37a3d-120">For acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="37a3d-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-121">Click **Add**.</span></span>
10. <span data-ttu-id="37a3d-122">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-122">In the **Book** field, enter or select a value.</span></span>
11. <span data-ttu-id="37a3d-123">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-123">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="37a3d-124">Hankintaoikaisuille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="37a3d-124">For acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="37a3d-125">Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poisto.</span><span class="sxs-lookup"><span data-stu-id="37a3d-125">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation'.</span></span>
13. <span data-ttu-id="37a3d-126">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-126">Click **Add**.</span></span>
14. <span data-ttu-id="37a3d-127">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-127">In the **Book** field, enter or select a value.</span></span>
15. <span data-ttu-id="37a3d-128">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-128">In the **Main account** field, specify the desired values.</span></span>
16. <span data-ttu-id="37a3d-129">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-129">In the **Offset account** field, specify the desired values.</span></span>
17. <span data-ttu-id="37a3d-130">Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistojen oikaisu.</span><span class="sxs-lookup"><span data-stu-id="37a3d-130">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation adjustment'.</span></span> <span data-ttu-id="37a3d-131">Poiston oikaisutapahtumissa käytetään samoja tilejä kuin poistotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="37a3d-131">For depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="37a3d-132">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-132">Click **Add**.</span></span>
19. <span data-ttu-id="37a3d-133">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-133">In the **Book** field, enter or select a value.</span></span>
20. <span data-ttu-id="37a3d-134">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-134">In the **Main account** field, specify the desired values.</span></span>
21. <span data-ttu-id="37a3d-135">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-135">In the **Offset account** field, specify the desired values.</span></span>
22. <span data-ttu-id="37a3d-136">Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistomyynti.</span><span class="sxs-lookup"><span data-stu-id="37a3d-136">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="37a3d-137">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-137">Click **Add**.</span></span>
24. <span data-ttu-id="37a3d-138">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-138">In the **Book** field, enter or select a value.</span></span>
25. <span data-ttu-id="37a3d-139">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-139">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="37a3d-140">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="37a3d-140">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="37a3d-141">Valitse **Kirjanpitotilit** -pikavälilehden avattavasta valikosta Poistohävikki.</span><span class="sxs-lookup"><span data-stu-id="37a3d-141">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - scrap'.</span></span> <span data-ttu-id="37a3d-142">Poistomyynnissä ja -hävikissä käytetään samoja tilejä.</span><span class="sxs-lookup"><span data-stu-id="37a3d-142">Use the same accounts for 'Disposal sale' and 'Disposal scrap'.</span></span>  
27. <span data-ttu-id="37a3d-143">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-143">Click **Add**.</span></span>
28. <span data-ttu-id="37a3d-144">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-144">In the **Book** field, enter or select a value.</span></span>
29. <span data-ttu-id="37a3d-145">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-145">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="37a3d-146">Poistoille voidaan syöttää vastatili tai jättää kohta tyhjäksi, jolloin sen täyttää tietty tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="37a3d-146">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="37a3d-147">Laajenna **Poisto**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="37a3d-147">Expand the **Disposal** fastTab.</span></span> <span data-ttu-id="37a3d-148">Määritä poiston kirjausprofiilit sekä myynnille että hävikille.</span><span class="sxs-lookup"><span data-stu-id="37a3d-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="37a3d-149">Aloitetaan poistomyyntitapahtumilla.</span><span class="sxs-lookup"><span data-stu-id="37a3d-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="37a3d-150">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-150">Click **Add**.</span></span>
32. <span data-ttu-id="37a3d-151">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-151">In the **Book** field, enter or select a value.</span></span>
33. <span data-ttu-id="37a3d-152">Valitse **Kirjausarvo**-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="37a3d-152">In the **Post value** field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="37a3d-153">Hankinta-arvo koskee kaikkien vuosien hankinta-arvoja ja hankinnan oikaisun arvoja.</span><span class="sxs-lookup"><span data-stu-id="37a3d-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span> <span data-ttu-id="37a3d-154">Voit myös määrittää tilit erikseen näille tapahtumalajeille.</span><span class="sxs-lookup"><span data-stu-id="37a3d-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="37a3d-155">Voit määrittää poistoprosessin käyttämään eri tilejä sen mukaan, onko poiston tuloksena voitto vai tappio.</span><span class="sxs-lookup"><span data-stu-id="37a3d-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span> <span data-ttu-id="37a3d-156">Määritetään myynnin arvon tyypiksi Kaikki. Tällöin samoja tilejä käytetään kaikissa poistotyypeissä.</span><span class="sxs-lookup"><span data-stu-id="37a3d-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="37a3d-157">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-157">In the **Main account** field, specify the desired values.</span></span>
35. <span data-ttu-id="37a3d-158">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-158">In the **Offset account** field, specify the desired values.</span></span>
36. <span data-ttu-id="37a3d-159">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-159">Click **Add**.</span></span>
37. <span data-ttu-id="37a3d-160">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-160">In the **Book** field, enter or select a value.</span></span>
38. <span data-ttu-id="37a3d-161">Valitse **Kirjausarvo**-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="37a3d-161">In the **Post value** field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="37a3d-162">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-162">In the **Main account** field, specify the desired values.</span></span>
39. <span data-ttu-id="37a3d-163">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-163">In the **Offset account** field, specify the desired values.</span></span>
40. <span data-ttu-id="37a3d-164">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-164">Click **Add**.</span></span>
41. <span data-ttu-id="37a3d-165">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-165">In the **Book** field, enter or select a value.</span></span>
42. <span data-ttu-id="37a3d-166">Valitse **Kirjausarvo**-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="37a3d-166">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="37a3d-167">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-167">In the **Main account** field, specify the desired values.</span></span>
44. <span data-ttu-id="37a3d-168">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-168">In the **Offset account** field, specify the desired values.</span></span>
45. <span data-ttu-id="37a3d-169">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-169">Click **Add**.</span></span>
46. <span data-ttu-id="37a3d-170">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-170">In the **Book** field, enter or select a value.</span></span>
47. <span data-ttu-id="37a3d-171">Valitse **Kirjausarvo**-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="37a3d-171">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="37a3d-172">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-172">In the **Main account** field, specify the desired values.</span></span>
49. <span data-ttu-id="37a3d-173">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-173">In the **Offset account** field, specify the desired values.</span></span>
50. <span data-ttu-id="37a3d-174">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-174">Click **Add**.</span></span>
51. <span data-ttu-id="37a3d-175">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-175">In the **Book** field, enter or select a value.</span></span>
52. <span data-ttu-id="37a3d-176">Valitse **Kirjausarvo**-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="37a3d-176">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="37a3d-177">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-177">In the **Main account** field, specify the desired values.</span></span>
54. <span data-ttu-id="37a3d-178">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-178">In the **Offset account** field, specify the desired values.</span></span>
55. <span data-ttu-id="37a3d-179">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-179">Click **Add**.</span></span>
56. <span data-ttu-id="37a3d-180">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-180">In the **Book** field, enter or select a value.</span></span>
57. <span data-ttu-id="37a3d-181">Valitse **Kirjausarvo**-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="37a3d-181">In the **Post value** field, select 'Net book value'.</span></span>
58. <span data-ttu-id="37a3d-182">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-182">In the **Main account** field, specify the desired values.</span></span>
59. <span data-ttu-id="37a3d-183">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-183">In the **Offset account** field, specify the desired values.</span></span>
60. <span data-ttu-id="37a3d-184">Valitse **Myynti tai hävikki** -kentässä Hävikki.</span><span class="sxs-lookup"><span data-stu-id="37a3d-184">In the **Sale or scrap** field, select 'Scrap'.</span></span>
61. <span data-ttu-id="37a3d-185">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-185">Click **Add**.</span></span>
62. <span data-ttu-id="37a3d-186">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-186">In the **Book** field, enter or select a value.</span></span>
63. <span data-ttu-id="37a3d-187">Valitse **Kirjausarvo**-kentässä Hankinnan arvo.</span><span class="sxs-lookup"><span data-stu-id="37a3d-187">In the **Post value** field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="37a3d-188">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-188">In the **Main account** field, specify the desired values.</span></span>
65. <span data-ttu-id="37a3d-189">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-189">In the **Offset account** field, specify the desired values.</span></span>
66. <span data-ttu-id="37a3d-190">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-190">Click **Add**.</span></span>
67. <span data-ttu-id="37a3d-191">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-191">In the **Book** field, enter or select a value.</span></span>
67. <span data-ttu-id="37a3d-192">Valitse **Kirjausarvo**-kentässä Poisto (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="37a3d-192">In **Post value** field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="37a3d-193">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-193">In the **Main account** field, specify the desired values.</span></span>
69. <span data-ttu-id="37a3d-194">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-194">In the **Offset account** field, specify the desired values.</span></span>
70. <span data-ttu-id="37a3d-195">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-195">Click **Add**.</span></span>
71. <span data-ttu-id="37a3d-196">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-196">In the **Book** field, enter or select a value.</span></span>
72. <span data-ttu-id="37a3d-197">Valitse **Kirjausarvo**-kentässä Poisto (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="37a3d-197">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="37a3d-198">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-198">In the **Main account** field, specify the desired values.</span></span>
74. <span data-ttu-id="37a3d-199">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-199">In the **Offset account** field, specify the desired values.</span></span>
75. <span data-ttu-id="37a3d-200">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-200">Click **Add**.</span></span>
76. <span data-ttu-id="37a3d-201">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-201">In the **Book** field, enter or select a value.</span></span>
77. <span data-ttu-id="37a3d-202">Valitse **Kirjausarvo**-kentässä Poiston oikaisut (edeltävät vuodet).</span><span class="sxs-lookup"><span data-stu-id="37a3d-202">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="37a3d-203">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-203">In the **Main account** field, specify the desired values.</span></span>
79. <span data-ttu-id="37a3d-204">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-204">In the **Offset account** field, specify the desired values.</span></span>
80. <span data-ttu-id="37a3d-205">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-205">Click **Add**.</span></span>
81. <span data-ttu-id="37a3d-206">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-206">In the **Book** field, enter or select a value.</span></span>
82. <span data-ttu-id="37a3d-207">Valitse **Kirjausarvo**-kentässä Poiston oikaisut (tämä vuosi).</span><span class="sxs-lookup"><span data-stu-id="37a3d-207">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="37a3d-208">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-208">In the **Main account** field, specify the desired values.</span></span>
84. <span data-ttu-id="37a3d-209">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-209">In the **Offset account** field, specify the desired values.</span></span>
85. <span data-ttu-id="37a3d-210">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-210">Click **Add**.</span></span>
86. <span data-ttu-id="37a3d-211">Syötä tai valitse arvo kentässä **Kirja**.</span><span class="sxs-lookup"><span data-stu-id="37a3d-211">In the **Book** field, enter or select a value.</span></span>
87. <span data-ttu-id="37a3d-212">Valitse **Kirjausarvo**-kentässä Nettokirjanpitoarvo.</span><span class="sxs-lookup"><span data-stu-id="37a3d-212">In the **Post value** field, select 'Net book value'.</span></span>
88. <span data-ttu-id="37a3d-213">Määritä **Päätili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-213">In the **Main account** field, specify the desired values.</span></span>
89. <span data-ttu-id="37a3d-214">Määritä **Vastatili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="37a3d-214">In the **Offset account** field, specify the desired values.</span></span>
