--- 
title: "Laskennan ja summien yhteenvedon laskutoimitusten käyttäminen sähköistä raportointia (ER) varten"
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
ms.openlocfilehash: 143856f65eaf1d6d667f4f7dfb229807da6f4ad8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="4542c-103">Laskennan ja summien yhteenvedon laskutoimitusten käyttäminen sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="4542c-103">Use computations to make the output for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4542c-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4542c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="4542c-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="4542c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4542c-106">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 2: Määritä laskelmat)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4542c-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="4542c-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="4542c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="4542c-108">Määritä raportti käyttämään laskenta- ja summaustietoja</span><span class="sxs-lookup"><span data-stu-id="4542c-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="4542c-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="4542c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4542c-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4542c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4542c-111">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="4542c-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="4542c-112">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="4542c-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="4542c-113">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="4542c-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="4542c-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="4542c-114">Click Designer.</span></span>
7. <span data-ttu-id="4542c-115">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="4542c-116">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="4542c-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="4542c-117">Lisää uusi tietolähde, joka noutaa tallennettujen lohkojen luettelon.</span><span class="sxs-lookup"><span data-stu-id="4542c-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="4542c-118">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="4542c-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="4542c-119">Kirjoita Nimi-kenttään "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="4542c-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="4542c-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="4542c-120">$BlocksList</span></span>  
11. <span data-ttu-id="4542c-121">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="4542c-121">Click Edit formula.</span></span>
12. <span data-ttu-id="4542c-122">Valitse puussa "Data collection functions\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="4542c-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="4542c-123">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="4542c-123">Click Add function.</span></span>
14. <span data-ttu-id="4542c-124">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4542c-124">Click Add data source.</span></span>
15. <span data-ttu-id="4542c-125">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', ".</span><span class="sxs-lookup"><span data-stu-id="4542c-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="4542c-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4542c-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="4542c-127">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', "*")".</span><span class="sxs-lookup"><span data-stu-id="4542c-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "*")'.</span></span>
    * <span data-ttu-id="4542c-128">COLLECTEDLIST('$BlockName', "*")</span><span class="sxs-lookup"><span data-stu-id="4542c-128">COLLECTEDLIST('$BlockName', "*")</span></span>  
17. <span data-ttu-id="4542c-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4542c-129">Click Save.</span></span>
    * <span data-ttu-id="4542c-130">Kuvio "*" tarkoittaa, että kaikki lohkot lisätään tämän tietueen luetteloon.</span><span class="sxs-lookup"><span data-stu-id="4542c-130">The pattern “*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="4542c-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4542c-131">Close the page.</span></span>
19. <span data-ttu-id="4542c-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4542c-132">Click OK.</span></span>
20. <span data-ttu-id="4542c-133">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-133">Click the Format tab.</span></span>
21. <span data-ttu-id="4542c-134">Valitse puussa "Intrastat\Data".</span><span class="sxs-lookup"><span data-stu-id="4542c-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="4542c-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="4542c-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="4542c-136">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="4542c-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="4542c-137">Syötä Nimi-kenttään "Summat lohkoittain".</span><span class="sxs-lookup"><span data-stu-id="4542c-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="4542c-138">Kokonaissummat lohkon mukaan</span><span class="sxs-lookup"><span data-stu-id="4542c-138">Totals by blocks</span></span>  
25. <span data-ttu-id="4542c-139">Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".</span><span class="sxs-lookup"><span data-stu-id="4542c-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="4542c-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4542c-140">Click OK.</span></span>
27. <span data-ttu-id="4542c-141">Valitse puussa solmu "Intrastat\Data\Totals by blocks".</span><span class="sxs-lookup"><span data-stu-id="4542c-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="4542c-142">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="4542c-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="4542c-143">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="4542c-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="4542c-144">Kirjoita Nimi-kenttään "Lohkokoodi".</span><span class="sxs-lookup"><span data-stu-id="4542c-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="4542c-145">Lohkon koodi</span><span class="sxs-lookup"><span data-stu-id="4542c-145">Block code</span></span>  
31. <span data-ttu-id="4542c-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4542c-146">Click OK.</span></span>
32. <span data-ttu-id="4542c-147">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4542c-147">Click Add String.</span></span>
33. <span data-ttu-id="4542c-148">Syötä Nimi-kenttään "Rivien laskenta".</span><span class="sxs-lookup"><span data-stu-id="4542c-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="4542c-149">Rivien laskenta</span><span class="sxs-lookup"><span data-stu-id="4542c-149">Lines counting</span></span>  
34. <span data-ttu-id="4542c-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4542c-150">Click OK.</span></span>
35. <span data-ttu-id="4542c-151">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4542c-151">Click Add String.</span></span>
36. <span data-ttu-id="4542c-152">Syötä Nimi-kenttään "Kokonaissumma".</span><span class="sxs-lookup"><span data-stu-id="4542c-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="4542c-153">Kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="4542c-153">Total amount</span></span>  
37. <span data-ttu-id="4542c-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4542c-154">Click OK.</span></span>
38. <span data-ttu-id="4542c-155">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="4542c-156">Valitse puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="4542c-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="4542c-157">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="4542c-157">Click Bind.</span></span>
    * <span data-ttu-id="4542c-158">Luo yhteenveto kullekin tallennetulle lohkolle.</span><span class="sxs-lookup"><span data-stu-id="4542c-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="4542c-159">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-159">Click the Format tab.</span></span>
42. <span data-ttu-id="4542c-160">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Block code".</span><span class="sxs-lookup"><span data-stu-id="4542c-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="4542c-161">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="4542c-162">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="4542c-162">Click Edit formula.</span></span>
45. <span data-ttu-id="4542c-163">Kirjoita kaava-kenttään "Block id: " & .</span><span class="sxs-lookup"><span data-stu-id="4542c-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="4542c-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="4542c-164">"Block id: " &</span></span>  
46. <span data-ttu-id="4542c-165">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="4542c-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="4542c-166">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="4542c-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="4542c-167">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4542c-167">Click Add data source.</span></span>
49. <span data-ttu-id="4542c-168">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4542c-168">Click Save.</span></span>
50. <span data-ttu-id="4542c-169">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4542c-169">Close the page.</span></span>
51. <span data-ttu-id="4542c-170">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-170">Click the Format tab.</span></span>
52. <span data-ttu-id="4542c-171">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Lines counting".</span><span class="sxs-lookup"><span data-stu-id="4542c-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="4542c-172">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="4542c-173">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="4542c-173">Click Edit formula.</span></span>
    * <span data-ttu-id="4542c-174">Luo tuotos kullekin tässä raportissa esitetyn lohkon rivimäärälle.</span><span class="sxs-lookup"><span data-stu-id="4542c-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="4542c-175">Kirjoita Kaava-kenttään "Number of lines in this block: " & .</span><span class="sxs-lookup"><span data-stu-id="4542c-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="4542c-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="4542c-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="4542c-177">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="4542c-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="4542c-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="4542c-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="4542c-179">Valitse puussa "Data collection functions\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="4542c-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="4542c-180">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="4542c-180">Click Add function.</span></span>
59. <span data-ttu-id="4542c-181">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4542c-181">Click Add data source.</span></span>
60. <span data-ttu-id="4542c-182">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="4542c-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="4542c-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4542c-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="4542c-184">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="4542c-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="4542c-185">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="4542c-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="4542c-186">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4542c-186">Click Add data source.</span></span>
64. <span data-ttu-id="4542c-187">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, .</span><span class="sxs-lookup"><span data-stu-id="4542c-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="4542c-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="4542c-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="4542c-189">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="4542c-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="4542c-190">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="4542c-190">Click Add data source.</span></span>
67. <span data-ttu-id="4542c-191">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="4542c-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="4542c-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="4542c-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
68. <span data-ttu-id="4542c-193">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4542c-193">Click Save.</span></span>
69. <span data-ttu-id="4542c-194">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4542c-194">Close the page.</span></span>
70. <span data-ttu-id="4542c-195">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-195">Click the Format tab.</span></span>
71. <span data-ttu-id="4542c-196">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Total amount".</span><span class="sxs-lookup"><span data-stu-id="4542c-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="4542c-197">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4542c-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="4542c-198">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="4542c-198">Click Edit formula.</span></span>
    * <span data-ttu-id="4542c-199">Luo tuotos, joka on kunkin tässä raportissa esitetyn lohkon yhteenlaskettu laskutussumma.</span><span class="sxs-lookup"><span data-stu-id="4542c-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="4542c-200">Kirjoita Kaava-kenttään "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="4542c-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="4542c-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="4542c-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
75. <span data-ttu-id="4542c-202">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4542c-202">Click Save.</span></span>
76. <span data-ttu-id="4542c-203">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4542c-203">Close the page.</span></span>
77. <span data-ttu-id="4542c-204">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4542c-204">Click Save.</span></span>
78. <span data-ttu-id="4542c-205">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4542c-205">Close the page.</span></span>


