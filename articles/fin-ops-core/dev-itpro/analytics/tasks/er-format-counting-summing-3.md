---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 3 – Tuotoksen luonti laskentojen avulla)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748994"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="7eec8-104">ER Määritä muoto suorittamaan laskenta ja summaus (Osa 3 – Tuotoksen luonti laskentojen avulla)</span><span class="sxs-lookup"><span data-stu-id="7eec8-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7eec8-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="7eec8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="7eec8-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="7eec8-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="7eec8-107">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 2: Määritä laskelmat)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="7eec8-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="7eec8-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="7eec8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="7eec8-109">Määritä raportti käyttämään laskenta- ja summaustietoja</span><span class="sxs-lookup"><span data-stu-id="7eec8-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="7eec8-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="7eec8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7eec8-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7eec8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7eec8-112">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="7eec8-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="7eec8-113">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="7eec8-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="7eec8-114">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="7eec8-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="7eec8-115">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="7eec8-115">Click Designer.</span></span>
7. <span data-ttu-id="7eec8-116">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="7eec8-117">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="7eec8-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="7eec8-118">Lisää uusi tietolähde, joka noutaa tallennettujen lohkojen luettelon.</span><span class="sxs-lookup"><span data-stu-id="7eec8-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="7eec8-119">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="7eec8-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="7eec8-120">Kirjoita Nimi-kenttään "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="7eec8-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="7eec8-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="7eec8-121">$BlocksList</span></span>  
11. <span data-ttu-id="7eec8-122">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="7eec8-122">Click Edit formula.</span></span>
12. <span data-ttu-id="7eec8-123">Valitse puussa "Data collection functions\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="7eec8-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="7eec8-124">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="7eec8-124">Click Add function.</span></span>
14. <span data-ttu-id="7eec8-125">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="7eec8-125">Click Add data source.</span></span>
15. <span data-ttu-id="7eec8-126">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', ".</span><span class="sxs-lookup"><span data-stu-id="7eec8-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="7eec8-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="7eec8-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="7eec8-128">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', "\*")".</span><span class="sxs-lookup"><span data-stu-id="7eec8-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="7eec8-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="7eec8-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="7eec8-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7eec8-130">Click Save.</span></span>
    * <span data-ttu-id="7eec8-131">Kuvio "\*" tarkoittaa, että kaikki lohkot lisätään tämän tietueen luetteloon.</span><span class="sxs-lookup"><span data-stu-id="7eec8-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="7eec8-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7eec8-132">Close the page.</span></span>
19. <span data-ttu-id="7eec8-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7eec8-133">Click OK.</span></span>
20. <span data-ttu-id="7eec8-134">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-134">Click the Format tab.</span></span>
21. <span data-ttu-id="7eec8-135">Valitse puussa "Intrastat\Data".</span><span class="sxs-lookup"><span data-stu-id="7eec8-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="7eec8-136">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7eec8-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="7eec8-137">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="7eec8-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="7eec8-138">Syötä Nimi-kenttään "Summat lohkoittain".</span><span class="sxs-lookup"><span data-stu-id="7eec8-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="7eec8-139">Kokonaissummat lohkon mukaan</span><span class="sxs-lookup"><span data-stu-id="7eec8-139">Totals by blocks</span></span>  
25. <span data-ttu-id="7eec8-140">Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".</span><span class="sxs-lookup"><span data-stu-id="7eec8-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="7eec8-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7eec8-141">Click OK.</span></span>
27. <span data-ttu-id="7eec8-142">Valitse puussa solmu "Intrastat\Data\Totals by blocks".</span><span class="sxs-lookup"><span data-stu-id="7eec8-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="7eec8-143">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7eec8-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="7eec8-144">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="7eec8-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="7eec8-145">Kirjoita Nimi-kenttään "Lohkokoodi".</span><span class="sxs-lookup"><span data-stu-id="7eec8-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="7eec8-146">Lohkon koodi</span><span class="sxs-lookup"><span data-stu-id="7eec8-146">Block code</span></span>  
31. <span data-ttu-id="7eec8-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7eec8-147">Click OK.</span></span>
32. <span data-ttu-id="7eec8-148">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="7eec8-148">Click Add String.</span></span>
33. <span data-ttu-id="7eec8-149">Syötä Nimi-kenttään "Rivien laskenta".</span><span class="sxs-lookup"><span data-stu-id="7eec8-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="7eec8-150">Rivien laskenta</span><span class="sxs-lookup"><span data-stu-id="7eec8-150">Lines counting</span></span>  
34. <span data-ttu-id="7eec8-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7eec8-151">Click OK.</span></span>
35. <span data-ttu-id="7eec8-152">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="7eec8-152">Click Add String.</span></span>
36. <span data-ttu-id="7eec8-153">Syötä Nimi-kenttään "Kokonaissumma".</span><span class="sxs-lookup"><span data-stu-id="7eec8-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="7eec8-154">Kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="7eec8-154">Total amount</span></span>  
37. <span data-ttu-id="7eec8-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7eec8-155">Click OK.</span></span>
38. <span data-ttu-id="7eec8-156">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="7eec8-157">Valitse puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="7eec8-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="7eec8-158">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7eec8-158">Click Bind.</span></span>
    * <span data-ttu-id="7eec8-159">Luo yhteenveto kullekin tallennetulle lohkolle.</span><span class="sxs-lookup"><span data-stu-id="7eec8-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="7eec8-160">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-160">Click the Format tab.</span></span>
42. <span data-ttu-id="7eec8-161">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Block code".</span><span class="sxs-lookup"><span data-stu-id="7eec8-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="7eec8-162">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="7eec8-163">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="7eec8-163">Click Edit formula.</span></span>
45. <span data-ttu-id="7eec8-164">Kirjoita kaava-kenttään "Block id: " & .</span><span class="sxs-lookup"><span data-stu-id="7eec8-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="7eec8-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="7eec8-165">"Block id: " &</span></span>  
46. <span data-ttu-id="7eec8-166">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="7eec8-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="7eec8-167">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="7eec8-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="7eec8-168">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="7eec8-168">Click Add data source.</span></span>
49. <span data-ttu-id="7eec8-169">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7eec8-169">Click Save.</span></span>
50. <span data-ttu-id="7eec8-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7eec8-170">Close the page.</span></span>
51. <span data-ttu-id="7eec8-171">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-171">Click the Format tab.</span></span>
52. <span data-ttu-id="7eec8-172">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Lines counting".</span><span class="sxs-lookup"><span data-stu-id="7eec8-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="7eec8-173">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="7eec8-174">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="7eec8-174">Click Edit formula.</span></span>
    * <span data-ttu-id="7eec8-175">Luo tuotos kullekin tässä raportissa esitetyn lohkon rivimäärälle.</span><span class="sxs-lookup"><span data-stu-id="7eec8-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="7eec8-176">Kirjoita Kaava-kenttään "Number of lines in this block: " & .</span><span class="sxs-lookup"><span data-stu-id="7eec8-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="7eec8-177">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="7eec8-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="7eec8-178">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="7eec8-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="7eec8-179">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="7eec8-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="7eec8-180">Valitse puussa "Data collection functions\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="7eec8-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="7eec8-181">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="7eec8-181">Click Add function.</span></span>
59. <span data-ttu-id="7eec8-182">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="7eec8-182">Click Add data source.</span></span>
60. <span data-ttu-id="7eec8-183">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="7eec8-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="7eec8-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="7eec8-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="7eec8-185">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="7eec8-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="7eec8-186">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="7eec8-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="7eec8-187">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="7eec8-187">Click Add data source.</span></span>
64. <span data-ttu-id="7eec8-188">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, .</span><span class="sxs-lookup"><span data-stu-id="7eec8-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="7eec8-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="7eec8-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="7eec8-190">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="7eec8-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="7eec8-191">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="7eec8-191">Click Add data source.</span></span>
67. <span data-ttu-id="7eec8-192">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="7eec8-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="7eec8-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="7eec8-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="7eec8-194">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7eec8-194">Click Save.</span></span>
69. <span data-ttu-id="7eec8-195">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7eec8-195">Close the page.</span></span>
70. <span data-ttu-id="7eec8-196">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-196">Click the Format tab.</span></span>
71. <span data-ttu-id="7eec8-197">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Total amount".</span><span class="sxs-lookup"><span data-stu-id="7eec8-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="7eec8-198">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7eec8-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="7eec8-199">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="7eec8-199">Click Edit formula.</span></span>
    * <span data-ttu-id="7eec8-200">Luo tuotos, joka on kunkin tässä raportissa esitetyn lohkon yhteenlaskettu laskutussumma.</span><span class="sxs-lookup"><span data-stu-id="7eec8-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="7eec8-201">Kirjoita Kaava-kenttään "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="7eec8-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="7eec8-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="7eec8-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="7eec8-203">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7eec8-203">Click Save.</span></span>
76. <span data-ttu-id="7eec8-204">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7eec8-204">Close the page.</span></span>
77. <span data-ttu-id="7eec8-205">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7eec8-205">Click Save.</span></span>
78. <span data-ttu-id="7eec8-206">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7eec8-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]