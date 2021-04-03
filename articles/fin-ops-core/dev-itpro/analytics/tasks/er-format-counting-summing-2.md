---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 2 – Laskentojen konfigurointi)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6eb3d686e8f60de51001deffb4c2460c181a4ab
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565162"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="85f94-104">ER Määritä muoto suorittamaan laskenta ja summaus (Osa 2 – Laskentojen konfigurointi)</span><span class="sxs-lookup"><span data-stu-id="85f94-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85f94-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="85f94-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="85f94-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="85f94-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="85f94-107">Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 1: Luo muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="85f94-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="85f94-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="85f94-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="85f94-109">Luo muotokonfiguraaio, jossa lisätään laskennan ja summauksen tiedot</span><span class="sxs-lookup"><span data-stu-id="85f94-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="85f94-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="85f94-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="85f94-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="85f94-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="85f94-112">Laajenna puussa solmu "Intrastat model".</span><span class="sxs-lookup"><span data-stu-id="85f94-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="85f94-113">Valitse puusta "Intrastat model\Intrastat (DE)"</span><span class="sxs-lookup"><span data-stu-id="85f94-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="85f94-114">Oletetaan, että sinun on mukautettava Microsoftin toimittamaa muotoa lisäämällä rivejä, jotka sisältävät yhteenvetotietoja Intrastat-raportin loppuun.</span><span class="sxs-lookup"><span data-stu-id="85f94-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="85f94-115">Muokkauksia voit tehdä johtamalla oman Intrastat-kokoonpanon Microsoftin tarjoamasta esiintymästä.</span><span class="sxs-lookup"><span data-stu-id="85f94-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="85f94-116">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="85f94-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="85f94-117">Kirjoita Uusi-kenttään "Derive from Name: Intrastat (DE), Microsoft".</span><span class="sxs-lookup"><span data-stu-id="85f94-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="85f94-118">Kirjoita Nimi-kenttään Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="85f94-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="85f94-119">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="85f94-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="85f94-120">Määritä raportin suorittamaan laskenta ja summaus tuotoksen perusteella</span><span class="sxs-lookup"><span data-stu-id="85f94-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="85f94-121">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="85f94-121">Click Designer.</span></span>
2. <span data-ttu-id="85f94-122">Valitse Kerää tulostiedot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="85f94-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="85f94-123">Tämä merkintä aktivoituu Intrastat-tiedoston luonnin tulostustietojen keräysprosessin suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="85f94-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="85f94-124">Laskenta on suoritettava useisiin Intrastat-suuntiin, joten lisää kohdistettu mallin luettelointi tämän muotokonfiguraation tietolähteiden luetteloon.</span><span class="sxs-lookup"><span data-stu-id="85f94-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="85f94-125">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="85f94-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="85f94-126">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="85f94-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="85f94-127">Valitse puussa solmu "Data model\Enumeration".</span><span class="sxs-lookup"><span data-stu-id="85f94-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="85f94-128">Kirjoita Nimi-kenttään "Suunta".</span><span class="sxs-lookup"><span data-stu-id="85f94-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="85f94-129">Syötä tai valitse arvo Mallin luettelointi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="85f94-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="85f94-130">Valitse arvoksi Siirtosuunta.</span><span class="sxs-lookup"><span data-stu-id="85f94-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="85f94-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85f94-131">Click OK.</span></span>
9. <span data-ttu-id="85f94-132">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="85f94-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="85f94-133">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="85f94-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="85f94-134">Kirjoita Nimi-kenttään "$BlockName".</span><span class="sxs-lookup"><span data-stu-id="85f94-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="85f94-135">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="85f94-135">Click Edit formula.</span></span>
13. <span data-ttu-id="85f94-136">Kirjoita Kaava-kenttään "block".</span><span class="sxs-lookup"><span data-stu-id="85f94-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="85f94-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-137">Click Save.</span></span>
15. <span data-ttu-id="85f94-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-138">Close the page.</span></span>
16. <span data-ttu-id="85f94-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85f94-139">Click OK.</span></span>
17. <span data-ttu-id="85f94-140">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="85f94-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="85f94-141">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="85f94-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="85f94-142">Kirjoita Nimi-kenttään "$RecName".</span><span class="sxs-lookup"><span data-stu-id="85f94-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="85f94-143">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="85f94-143">Click Edit formula.</span></span>
21. <span data-ttu-id="85f94-144">Kirjoita Kaava-kenttään "record".</span><span class="sxs-lookup"><span data-stu-id="85f94-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="85f94-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-145">Click Save.</span></span>
23. <span data-ttu-id="85f94-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-146">Close the page.</span></span>
24. <span data-ttu-id="85f94-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85f94-147">Click OK.</span></span>
25. <span data-ttu-id="85f94-148">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="85f94-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="85f94-149">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="85f94-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="85f94-150">Kirjoita Nimi-kenttään "$InvName".</span><span class="sxs-lookup"><span data-stu-id="85f94-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="85f94-151">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="85f94-151">Click Edit formula.</span></span>
29. <span data-ttu-id="85f94-152">Kirjoita Kaava-kenttään "InvoicedAmountEUR".</span><span class="sxs-lookup"><span data-stu-id="85f94-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="85f94-153">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-153">Click Save.</span></span>
31. <span data-ttu-id="85f94-154">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-154">Close the page.</span></span>
32. <span data-ttu-id="85f94-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85f94-155">Click OK.</span></span>
33. <span data-ttu-id="85f94-156">Valitse puussa "Intrastat\Data".</span><span class="sxs-lookup"><span data-stu-id="85f94-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="85f94-157">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike</span><span class="sxs-lookup"><span data-stu-id="85f94-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="85f94-158">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="85f94-158">Click Add data source.</span></span>
    * <span data-ttu-id="85f94-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="85f94-159">$BlockName</span></span>  
36. <span data-ttu-id="85f94-160">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-160">Click Save.</span></span>
37. <span data-ttu-id="85f94-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-161">Close the page.</span></span>
38. <span data-ttu-id="85f94-162">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="85f94-163">Kirjoita Kaava-kenttään "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".</span><span class="sxs-lookup"><span data-stu-id="85f94-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="85f94-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="85f94-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="85f94-165">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-165">Click Save.</span></span>
41. <span data-ttu-id="85f94-166">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-166">Close the page.</span></span>
    * <span data-ttu-id="85f94-167">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="85f94-167">Count the lines of this sequence.</span></span> <span data-ttu-id="85f94-168">Tuloksia käytetään nimellä "lohko" erikseen eri suunnille.</span><span class="sxs-lookup"><span data-stu-id="85f94-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="85f94-169">"Tuonti"-arvoa käytetään kaikille saapuville Intrastat-tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="85f94-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="85f94-170">"Vienti"-arvoa käytetään kaikille lähteville Intrastat-tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="85f94-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="85f94-171">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="85f94-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="85f94-172">Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti".</span><span class="sxs-lookup"><span data-stu-id="85f94-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="85f94-173">Laajenna puussa solmu "Intrastat\Data: Sequence".</span><span class="sxs-lookup"><span data-stu-id="85f94-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="85f94-174">Valitse puussa solmu "Intrastat\Data Sequence\Arrivals?".</span><span class="sxs-lookup"><span data-stu-id="85f94-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="85f94-175">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="85f94-176">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="85f94-176">Count the lines of this sequence.</span></span> <span data-ttu-id="85f94-177">Tulokset tallennetaan nimellä "tietue".</span><span class="sxs-lookup"><span data-stu-id="85f94-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="85f94-178">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="85f94-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="85f94-179">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="85f94-179">Click Add data source.</span></span>
47. <span data-ttu-id="85f94-180">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-180">Click Save.</span></span>
48. <span data-ttu-id="85f94-181">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-181">Close the page.</span></span>
49. <span data-ttu-id="85f94-182">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="85f94-183">Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="85f94-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="85f94-184">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-184">Click Save.</span></span>
52. <span data-ttu-id="85f94-185">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-185">Close the page.</span></span>
    * <span data-ttu-id="85f94-186">Laske tämän sarjan rivit..</span><span class="sxs-lookup"><span data-stu-id="85f94-186">Count the lines of this sequence.</span></span> <span data-ttu-id="85f94-187">Tuloksia käytetään nimellä "tietue" erikseen eri kauppatavarakoodeille.</span><span class="sxs-lookup"><span data-stu-id="85f94-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="85f94-188">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="85f94-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="85f94-189">Kullakin tapahtumalla on rivi, jossa ensimmäinen sarakelohko täytetään vastaavasti arvoilla "Tuonti" ja "Vienti" vastaavasti ja toinen lohkotietue täytetään kauppatavarakoodeilla.</span><span class="sxs-lookup"><span data-stu-id="85f94-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="85f94-190">Valitse puussa solmu "Intrastat\Data Sequence\Dispatches?".</span><span class="sxs-lookup"><span data-stu-id="85f94-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="85f94-191">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike</span><span class="sxs-lookup"><span data-stu-id="85f94-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="85f94-192">Valitse puussa "$RecName".</span><span class="sxs-lookup"><span data-stu-id="85f94-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="85f94-193">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="85f94-193">Click Add data source.</span></span>
57. <span data-ttu-id="85f94-194">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-194">Click Save.</span></span>
58. <span data-ttu-id="85f94-195">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-195">Close the page.</span></span>
59. <span data-ttu-id="85f94-196">Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="85f94-197">Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="85f94-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="85f94-198">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-198">Click Save.</span></span>
62. <span data-ttu-id="85f94-199">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-199">Close the page.</span></span>
63. <span data-ttu-id="85f94-200">Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?".</span><span class="sxs-lookup"><span data-stu-id="85f94-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="85f94-201">Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="85f94-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="85f94-202">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="85f94-202">Click the Format tab.</span></span>
66. <span data-ttu-id="85f94-203">Valitse puussa "Intrastat\Data\Dispatches\Record\Invoice amount EUR".</span><span class="sxs-lookup"><span data-stu-id="85f94-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="85f94-204">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="85f94-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="85f94-205">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="85f94-206">Valitse puussa "$InvName".</span><span class="sxs-lookup"><span data-stu-id="85f94-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="85f94-207">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="85f94-207">Click Add data source.</span></span>
71. <span data-ttu-id="85f94-208">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-208">Click Save.</span></span>
72. <span data-ttu-id="85f94-209">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-209">Close the page.</span></span>
    * <span data-ttu-id="85f94-210">Tee yhteenveto tämän sarjan riveillä laskutetuille summille.</span><span class="sxs-lookup"><span data-stu-id="85f94-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="85f94-211">Tuloksia käytetään nimellä "InvoicedAmountEUR" erikseen eri Intrastat-suunnille ja kauppatavarakoodeille.</span><span class="sxs-lookup"><span data-stu-id="85f94-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="85f94-212">Ajattele tätä virtuaalisena Excel-taulukkona.</span><span class="sxs-lookup"><span data-stu-id="85f94-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="85f94-213">Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti".</span><span class="sxs-lookup"><span data-stu-id="85f94-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="85f94-214">Toiseen tietuelohkoon täytetään kauppatavarakoodin arvo ja kolmanteen sarakkeeseen, "InvoicedAmountEUR" tulee laskutussumman arvo.</span><span class="sxs-lookup"><span data-stu-id="85f94-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="85f94-215">Laajenna puussa solmu "Intrastat\Data\Arrivals?".</span><span class="sxs-lookup"><span data-stu-id="85f94-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="85f94-216">Laajenna puussa "Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord".</span><span class="sxs-lookup"><span data-stu-id="85f94-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="85f94-217">Valitse Muoto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="85f94-217">Click the Format tab.</span></span>
76. <span data-ttu-id="85f94-218">Valitse puussa "Intrastat\Data\Arrivals\Record\Invoice amount EUR".</span><span class="sxs-lookup"><span data-stu-id="85f94-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="85f94-219">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="85f94-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="85f94-220">Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.</span><span class="sxs-lookup"><span data-stu-id="85f94-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="85f94-221">Valitse puussa "$InvName".</span><span class="sxs-lookup"><span data-stu-id="85f94-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="85f94-222">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="85f94-222">Click Add data source.</span></span>
81. <span data-ttu-id="85f94-223">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-223">Click Save.</span></span>
82. <span data-ttu-id="85f94-224">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-224">Close the page.</span></span>
83. <span data-ttu-id="85f94-225">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85f94-225">Click Save.</span></span>
84. <span data-ttu-id="85f94-226">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="85f94-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]