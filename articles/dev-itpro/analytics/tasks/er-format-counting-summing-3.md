---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 3 – Tuotoksen luonti laskentojen avulla)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "347074"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="6cbc4-103">ER Määritä muoto suorittamaan laskenta ja summaus (osa 3: tuotoksen luonti laskentojen avulla)</span><span class="sxs-lookup"><span data-stu-id="6cbc4-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cbc4-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6cbc4-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6cbc4-106">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 2: Määritä laskelmat)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="6cbc4-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="6cbc4-108">Määritä raportti käyttämään laskenta- ja summaustietoja</span><span class="sxs-lookup"><span data-stu-id="6cbc4-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="6cbc4-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6cbc4-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6cbc4-111">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="6cbc4-112">Laajenna puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="6cbc4-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="6cbc4-113">Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="6cbc4-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-114">Click Designer.</span></span>
7. <span data-ttu-id="6cbc4-115">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="6cbc4-116">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="6cbc4-117">Lisää uusi tietolähde, joka noutaa tallennettujen lohkojen luettelon.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="6cbc4-118">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="6cbc4-119">Kirjoita Nimi-kenttään "$BlocksList".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="6cbc4-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="6cbc4-120">$BlocksList</span></span>  
11. <span data-ttu-id="6cbc4-121">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-121">Click Edit formula.</span></span>
12. <span data-ttu-id="6cbc4-122">Valitse puussa "Data collection functions\COLLECTEDLIST".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="6cbc4-123">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-123">Click Add function.</span></span>
14. <span data-ttu-id="6cbc4-124">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-124">Click Add data source.</span></span>
15. <span data-ttu-id="6cbc4-125">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', ".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="6cbc4-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6cbc4-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="6cbc4-127">Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', "\*")".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="6cbc4-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="6cbc4-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="6cbc4-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-129">Click Save.</span></span>
    * <span data-ttu-id="6cbc4-130">Kuvio "\*" tarkoittaa, että kaikki lohkot lisätään tämän tietueen luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="6cbc4-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-131">Close the page.</span></span>
19. <span data-ttu-id="6cbc4-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-132">Click OK.</span></span>
20. <span data-ttu-id="6cbc4-133">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-133">Click the Format tab.</span></span>
21. <span data-ttu-id="6cbc4-134">Valitse puussa "Intrastat\Data".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="6cbc4-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6cbc4-136">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="6cbc4-137">Syötä Nimi-kenttään "Summat lohkoittain".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="6cbc4-138">Kokonaissummat lohkon mukaan</span><span class="sxs-lookup"><span data-stu-id="6cbc4-138">Totals by blocks</span></span>  
25. <span data-ttu-id="6cbc4-139">Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="6cbc4-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-140">Click OK.</span></span>
27. <span data-ttu-id="6cbc4-141">Valitse puussa solmu "Intrastat\Data\Totals by blocks".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="6cbc4-142">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="6cbc4-143">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="6cbc4-144">Kirjoita Nimi-kenttään "Lohkokoodi".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="6cbc4-145">Lohkon koodi</span><span class="sxs-lookup"><span data-stu-id="6cbc4-145">Block code</span></span>  
31. <span data-ttu-id="6cbc4-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-146">Click OK.</span></span>
32. <span data-ttu-id="6cbc4-147">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-147">Click Add String.</span></span>
33. <span data-ttu-id="6cbc4-148">Syötä Nimi-kenttään "Rivien laskenta".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="6cbc4-149">Rivien laskenta</span><span class="sxs-lookup"><span data-stu-id="6cbc4-149">Lines counting</span></span>  
34. <span data-ttu-id="6cbc4-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-150">Click OK.</span></span>
35. <span data-ttu-id="6cbc4-151">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-151">Click Add String.</span></span>
36. <span data-ttu-id="6cbc4-152">Syötä Nimi-kenttään "Kokonaissumma".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="6cbc4-153">Kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="6cbc4-153">Total amount</span></span>  
37. <span data-ttu-id="6cbc4-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-154">Click OK.</span></span>
38. <span data-ttu-id="6cbc4-155">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="6cbc4-156">Valitse puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="6cbc4-157">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-157">Click Bind.</span></span>
    * <span data-ttu-id="6cbc4-158">Luo yhteenveto kullekin tallennetulle lohkolle.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="6cbc4-159">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-159">Click the Format tab.</span></span>
42. <span data-ttu-id="6cbc4-160">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Block code".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="6cbc4-161">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="6cbc4-162">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-162">Click Edit formula.</span></span>
45. <span data-ttu-id="6cbc4-163">Kirjoita kaava-kenttään "Block id: " & .</span><span class="sxs-lookup"><span data-stu-id="6cbc4-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="6cbc4-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="6cbc4-164">"Block id: " &</span></span>  
46. <span data-ttu-id="6cbc4-165">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="6cbc4-166">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="6cbc4-167">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-167">Click Add data source.</span></span>
49. <span data-ttu-id="6cbc4-168">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-168">Click Save.</span></span>
50. <span data-ttu-id="6cbc4-169">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-169">Close the page.</span></span>
51. <span data-ttu-id="6cbc4-170">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-170">Click the Format tab.</span></span>
52. <span data-ttu-id="6cbc4-171">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Lines counting".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="6cbc4-172">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="6cbc4-173">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-173">Click Edit formula.</span></span>
    * <span data-ttu-id="6cbc4-174">Luo tuotos kullekin tässä raportissa esitetyn lohkon rivimäärälle.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="6cbc4-175">Kirjoita Kaava-kenttään "Number of lines in this block: " & .</span><span class="sxs-lookup"><span data-stu-id="6cbc4-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="6cbc4-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="6cbc4-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="6cbc4-177">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="6cbc4-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="6cbc4-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="6cbc4-179">Valitse puussa "Data collection functions\COUNTIFS".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="6cbc4-180">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-180">Click Add function.</span></span>
59. <span data-ttu-id="6cbc4-181">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-181">Click Add data source.</span></span>
60. <span data-ttu-id="6cbc4-182">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="6cbc4-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="6cbc4-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6cbc4-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="6cbc4-184">Laajenna puussa '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="6cbc4-185">Valitse puussa '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="6cbc4-186">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-186">Click Add data source.</span></span>
64. <span data-ttu-id="6cbc4-187">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, .</span><span class="sxs-lookup"><span data-stu-id="6cbc4-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="6cbc4-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="6cbc4-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="6cbc4-189">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="6cbc4-190">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-190">Click Add data source.</span></span>
67. <span data-ttu-id="6cbc4-191">Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="6cbc4-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6cbc4-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6cbc4-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="6cbc4-193">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-193">Click Save.</span></span>
69. <span data-ttu-id="6cbc4-194">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-194">Close the page.</span></span>
70. <span data-ttu-id="6cbc4-195">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-195">Click the Format tab.</span></span>
71. <span data-ttu-id="6cbc4-196">Valitse puussa solmu "Intrastat\Data\Totals by blocks\Total amount".</span><span class="sxs-lookup"><span data-stu-id="6cbc4-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="6cbc4-197">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="6cbc4-198">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-198">Click Edit formula.</span></span>
    * <span data-ttu-id="6cbc4-199">Luo tuotos, joka on kunkin tässä raportissa esitetyn lohkon yhteenlaskettu laskutussumma.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="6cbc4-200">Kirjoita Kaava-kenttään "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="6cbc4-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6cbc4-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="6cbc4-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="6cbc4-202">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-202">Click Save.</span></span>
76. <span data-ttu-id="6cbc4-203">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-203">Close the page.</span></span>
77. <span data-ttu-id="6cbc4-204">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-204">Click Save.</span></span>
78. <span data-ttu-id="6cbc4-205">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6cbc4-205">Close the page.</span></span>

