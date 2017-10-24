--- 
title: "Laskennan ja summien yhteenvedon laskutoimitusten konfiguroiminen sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7b9035d8e7baf3c7ecb063b104b9a567be60840
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="configure-computations-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="135a0-103">Laskennan ja summien yhteenvedon laskutoimitusten konfiguroiminen sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="135a0-103">Configure computations to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="135a0-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="135a0-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="135a0-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="135a0-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="135a0-106">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 1: Luo muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="135a0-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="135a0-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="135a0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="135a0-108">Luo muotokonfiguraaio, jossa lisätään laskennan ja summauksen tiedot</span><span class="sxs-lookup"><span data-stu-id="135a0-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="135a0-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="135a0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="135a0-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="135a0-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="135a0-111">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="135a0-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="135a0-112">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="135a0-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="135a0-113">Oletetaan, että sinun on mukautettava Microsoftin toimittamaa muotoa lisäämällä rivejä, jotka sisältävät yhteenvetotietoja Intrastat-raportin loppuun.</span><span class="sxs-lookup"><span data-stu-id="135a0-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="135a0-114">Muokkauksia voit tehdä johtamalla oman Intrastat-kokoonpanon Microsoftin tarjoamasta esiintymästä.</span><span class="sxs-lookup"><span data-stu-id="135a0-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="135a0-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="135a0-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="135a0-116">Kirjoita Uusi-kenttään "Derive from Name: Intrastat (DE), Microsoft".</span><span class="sxs-lookup"><span data-stu-id="135a0-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="135a0-117">Kirjoita Nimi-kenttään Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="135a0-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="135a0-118">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="135a0-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="135a0-119">Määritä raportin suorittamaan laskenta ja summaus tuotoksen perusteella</span><span class="sxs-lookup"><span data-stu-id="135a0-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="135a0-120">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="135a0-120">Click Designer.</span></span>
2. <span data-ttu-id="135a0-121">Valitse Kerää tulostiedot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="135a0-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="135a0-122">Tämä merkintä aktivoituu Intrastat-tiedoston luonnin tulostustietojen keräysprosessin suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="135a0-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="135a0-123">Laskenta on suoritettava useisiin Intrastat-suuntiin, joten lisää kohdistettu mallin luettelointi tämän muotokonfiguraation tietolähteiden luetteloon.</span><span class="sxs-lookup"><span data-stu-id="135a0-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="135a0-124">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="135a0-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="135a0-125">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="135a0-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="135a0-126">Valitse puussa solmu "Data model\Enumeration".</span><span class="sxs-lookup"><span data-stu-id="135a0-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="135a0-127">Kirjoita Nimi-kenttään "Suunta".</span><span class="sxs-lookup"><span data-stu-id="135a0-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="135a0-128">Syötä tai valitse arvo Mallin luettelointi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="135a0-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="135a0-129">Valitse arvoksi Siirtosuunta.</span><span class="sxs-lookup"><span data-stu-id="135a0-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="135a0-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="135a0-130">Click OK.</span></span>
9. <span data-ttu-id="135a0-131">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="135a0-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="135a0-132">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="135a0-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="135a0-133">Kirjoita Nimi-kenttään "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="135a0-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="135a0-134">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="135a0-134">Click Edit formula.</span></span>
13. <span data-ttu-id="135a0-135">Kirjoita Kaava-kenttään "block".</span><span class="sxs-lookup"><span data-stu-id="135a0-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="135a0-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-136">Click Save.</span></span>
15. <span data-ttu-id="135a0-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-137">Close the page.</span></span>
16. <span data-ttu-id="135a0-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="135a0-138">Click OK.</span></span>
17. <span data-ttu-id="135a0-139">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="135a0-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="135a0-140">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="135a0-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="135a0-141">Kirjoita Nimi-kenttään "$RecName".</span><span class="sxs-lookup"><span data-stu-id="135a0-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="135a0-142">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="135a0-142">Click Edit formula.</span></span>
21. <span data-ttu-id="135a0-143">Kirjoita Kaava-kenttään "record".</span><span class="sxs-lookup"><span data-stu-id="135a0-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="135a0-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-144">Click Save.</span></span>
23. <span data-ttu-id="135a0-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-145">Close the page.</span></span>
24. <span data-ttu-id="135a0-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="135a0-146">Click OK.</span></span>
25. <span data-ttu-id="135a0-147">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="135a0-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="135a0-148">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="135a0-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="135a0-149">Kirjoita Nimi-kenttään "$InvName".</span><span class="sxs-lookup"><span data-stu-id="135a0-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="135a0-150">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="135a0-150">Click Edit formula.</span></span>
29. <span data-ttu-id="135a0-151">Kirjoita Kaava-kenttään "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="135a0-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="135a0-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-152">Click Save.</span></span>
31. <span data-ttu-id="135a0-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-153">Close the page.</span></span>
32. <span data-ttu-id="135a0-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="135a0-154">Click OK.</span></span>
33. <span data-ttu-id="135a0-155">Valitse puussa "Intrastat\Data".</span><span class="sxs-lookup"><span data-stu-id="135a0-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="135a0-156">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="135a0-157">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="135a0-157">Click Add data source.</span></span>
    * <span data-ttu-id="135a0-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="135a0-158">$BlockName</span></span>  
36. <span data-ttu-id="135a0-159">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-159">Click Save.</span></span>
37. <span data-ttu-id="135a0-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-160">Close the page.</span></span>
38. <span data-ttu-id="135a0-161">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="135a0-162">Kirjoita Kaava-kenttään "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".</span><span class="sxs-lookup"><span data-stu-id="135a0-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="135a0-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="135a0-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="135a0-164">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-164">Click Save.</span></span>
41. <span data-ttu-id="135a0-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-165">Close the page.</span></span>
    * <span data-ttu-id="135a0-166">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="135a0-166">Count the lines of this sequence.</span></span> <span data-ttu-id="135a0-167">Tuloksia käytetään nimellä "lohko" erikseen eri suunnille.</span><span class="sxs-lookup"><span data-stu-id="135a0-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="135a0-168">"Tuonti"-arvoa käytetään kaikille saapuville Intrastat-tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="135a0-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="135a0-169">"Vienti"-arvoa käytetään kaikille lähteville Intrastat-tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="135a0-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="135a0-170">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="135a0-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="135a0-171">Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti".</span><span class="sxs-lookup"><span data-stu-id="135a0-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="135a0-172">Laajenna puussa solmu "Intrastat\Data: Sequence".</span><span class="sxs-lookup"><span data-stu-id="135a0-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="135a0-173">Valitse puussa solmu "Intrastat\Data Sequence\Arrivals?".</span><span class="sxs-lookup"><span data-stu-id="135a0-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="135a0-174">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="135a0-175">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="135a0-175">Count the lines of this sequence.</span></span> <span data-ttu-id="135a0-176">Tulokset tallennetaan nimellä "tietue".</span><span class="sxs-lookup"><span data-stu-id="135a0-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="135a0-177">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="135a0-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="135a0-178">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="135a0-178">Click Add data source.</span></span>
47. <span data-ttu-id="135a0-179">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-179">Click Save.</span></span>
48. <span data-ttu-id="135a0-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-180">Close the page.</span></span>
49. <span data-ttu-id="135a0-181">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="135a0-182">Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="135a0-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="135a0-183">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-183">Click Save.</span></span>
52. <span data-ttu-id="135a0-184">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-184">Close the page.</span></span>
    * <span data-ttu-id="135a0-185">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="135a0-185">Count the lines of this sequence.</span></span> <span data-ttu-id="135a0-186">Tuloksia käytetään nimellä "tietue" erikseen eri kauppatavarakoodeille.</span><span class="sxs-lookup"><span data-stu-id="135a0-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="135a0-187">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="135a0-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="135a0-188">Kullakin tapahtumalla on rivi, jossa ensimmäinen sarakelohko täytetään vastaavasti arvoilla "Tuonti" ja "Vienti" vastaavasti ja toinen lohkotietue täytetään kauppatavarakoodeilla.</span><span class="sxs-lookup"><span data-stu-id="135a0-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="135a0-189">Valitse puussa solmu "Intrastat\Data Sequence\Dispatches?".</span><span class="sxs-lookup"><span data-stu-id="135a0-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="135a0-190">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="135a0-191">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="135a0-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="135a0-192">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="135a0-192">Click Add data source.</span></span>
57. <span data-ttu-id="135a0-193">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-193">Click Save.</span></span>
58. <span data-ttu-id="135a0-194">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-194">Close the page.</span></span>
59. <span data-ttu-id="135a0-195">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="135a0-196">Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="135a0-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="135a0-197">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-197">Click Save.</span></span>
62. <span data-ttu-id="135a0-198">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-198">Close the page.</span></span>
63. <span data-ttu-id="135a0-199">Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?".</span><span class="sxs-lookup"><span data-stu-id="135a0-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="135a0-200">Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="135a0-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="135a0-201">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="135a0-201">Click the Format tab.</span></span>
66. <span data-ttu-id="135a0-202">Valitse puussa "Intrastat\Data\Dispatches\Record\Invoice amount EUR".</span><span class="sxs-lookup"><span data-stu-id="135a0-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="135a0-203">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="135a0-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="135a0-204">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="135a0-205">Valitse puussa "$InvName".</span><span class="sxs-lookup"><span data-stu-id="135a0-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="135a0-206">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="135a0-206">Click Add data source.</span></span>
71. <span data-ttu-id="135a0-207">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-207">Click Save.</span></span>
72. <span data-ttu-id="135a0-208">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-208">Close the page.</span></span>
    * <span data-ttu-id="135a0-209">Tee yhteenveto tämän sarjan riveillä laskutetuille summille.</span><span class="sxs-lookup"><span data-stu-id="135a0-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="135a0-210">Tuloksia käytetään nimellä "InvoicedAmountEUR" erikseen eri Intrastat-suunnille ja kauppatavarakoodeille.</span><span class="sxs-lookup"><span data-stu-id="135a0-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="135a0-211">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="135a0-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="135a0-212">Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti".</span><span class="sxs-lookup"><span data-stu-id="135a0-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="135a0-213">Toiseen tietuelohkoon täytetään kauppatavarakoodin arvo ja kolmanteen sarakkeeseen, "InvoicedAmountEUR" tulee laskutussumman arvo.</span><span class="sxs-lookup"><span data-stu-id="135a0-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="135a0-214">Laajenna puussa solmu "Intrastat\Data\Arrivals?".</span><span class="sxs-lookup"><span data-stu-id="135a0-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="135a0-215">Laajenna puussa "Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="135a0-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="135a0-216">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="135a0-216">Click the Format tab.</span></span>
76. <span data-ttu-id="135a0-217">Valitse puussa "Intrastat\Data\Arrivals\Record\Invoice amount EUR".</span><span class="sxs-lookup"><span data-stu-id="135a0-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="135a0-218">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="135a0-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="135a0-219">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="135a0-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="135a0-220">Valitse puussa "$InvName".</span><span class="sxs-lookup"><span data-stu-id="135a0-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="135a0-221">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="135a0-221">Click Add data source.</span></span>
81. <span data-ttu-id="135a0-222">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-222">Click Save.</span></span>
82. <span data-ttu-id="135a0-223">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-223">Close the page.</span></span>
83. <span data-ttu-id="135a0-224">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="135a0-224">Click Save.</span></span>
84. <span data-ttu-id="135a0-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135a0-225">Close the page.</span></span>


