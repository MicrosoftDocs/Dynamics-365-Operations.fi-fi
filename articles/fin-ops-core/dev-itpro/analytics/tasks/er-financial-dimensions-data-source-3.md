---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 3)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752409"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="38eeb-104">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="38eeb-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38eeb-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="38eeb-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="38eeb-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="38eeb-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="38eeb-107">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="38eeb-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="38eeb-108">Suunnittele raportti, jossa esitetään taloushallinnon dimensioita</span><span class="sxs-lookup"><span data-stu-id="38eeb-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="38eeb-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="38eeb-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="38eeb-110">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="38eeb-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="38eeb-111">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="38eeb-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="38eeb-112">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="38eeb-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="38eeb-113">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="38eeb-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="38eeb-114">Kirjoita Nimi-kenttään Kirjauskansioraportti.</span><span class="sxs-lookup"><span data-stu-id="38eeb-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="38eeb-115">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="38eeb-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="38eeb-116">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="38eeb-116">Click Create configuration.</span></span>
8. <span data-ttu-id="38eeb-117">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="38eeb-117">Click Designer.</span></span>
9. <span data-ttu-id="38eeb-118">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="38eeb-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="38eeb-119">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="38eeb-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="38eeb-120">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="38eeb-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="38eeb-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-121">Click OK.</span></span>
13. <span data-ttu-id="38eeb-122">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="38eeb-123">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="38eeb-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="38eeb-124">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="38eeb-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="38eeb-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-125">Click OK.</span></span>
17. <span data-ttu-id="38eeb-126">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="38eeb-127">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="38eeb-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="38eeb-128">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="38eeb-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="38eeb-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-129">Click OK.</span></span>
21. <span data-ttu-id="38eeb-130">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="38eeb-131">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="38eeb-132">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="38eeb-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="38eeb-133">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="38eeb-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="38eeb-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-134">Click OK.</span></span>
26. <span data-ttu-id="38eeb-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="38eeb-136">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="38eeb-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="38eeb-137">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="38eeb-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="38eeb-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-138">Click OK.</span></span>
30. <span data-ttu-id="38eeb-139">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="38eeb-140">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="38eeb-141">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="38eeb-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="38eeb-142">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="38eeb-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="38eeb-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-143">Click OK.</span></span>
35. <span data-ttu-id="38eeb-144">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="38eeb-145">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="38eeb-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="38eeb-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-146">Click OK.</span></span>
38. <span data-ttu-id="38eeb-147">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="38eeb-148">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="38eeb-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="38eeb-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-149">Click OK.</span></span>
41. <span data-ttu-id="38eeb-150">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="38eeb-151">Kirjoita Nimi-kenttään "Dt".</span><span class="sxs-lookup"><span data-stu-id="38eeb-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="38eeb-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-152">Click OK.</span></span>
44. <span data-ttu-id="38eeb-153">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="38eeb-154">Kirjoita Nimi-kenttään "Ct".</span><span class="sxs-lookup"><span data-stu-id="38eeb-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="38eeb-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-155">Click OK.</span></span>
47. <span data-ttu-id="38eeb-156">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="38eeb-157">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="38eeb-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="38eeb-158">Kirjoita Nimi-kenttään "Dimensiot".</span><span class="sxs-lookup"><span data-stu-id="38eeb-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="38eeb-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-159">Click OK.</span></span>
51. <span data-ttu-id="38eeb-160">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="38eeb-161">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="38eeb-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="38eeb-162">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="38eeb-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="38eeb-163">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="38eeb-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="38eeb-164">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-164">Click OK.</span></span>
56. <span data-ttu-id="38eeb-165">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="38eeb-166">Kirjoita Nimi-kenttään "Arvo".</span><span class="sxs-lookup"><span data-stu-id="38eeb-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="38eeb-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-167">Click OK.</span></span>
59. <span data-ttu-id="38eeb-168">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="38eeb-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="38eeb-169">Kirjoita Nimi-kenttään. "Kuv."</span><span class="sxs-lookup"><span data-stu-id="38eeb-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="38eeb-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38eeb-170">Click OK.</span></span>
<span data-ttu-id="38eeb-171">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="38eeb-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="38eeb-172">Yhdistä raportin osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="38eeb-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="38eeb-173">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="38eeb-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="38eeb-174">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="38eeb-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="38eeb-175">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="38eeb-176">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="38eeb-177">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="38eeb-178">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="38eeb-179">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="38eeb-180">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-180">Click Bind.</span></span>
9. <span data-ttu-id="38eeb-181">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="38eeb-182">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="38eeb-183">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-183">Click Bind.</span></span>
12. <span data-ttu-id="38eeb-184">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="38eeb-185">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="38eeb-186">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-186">Click Bind.</span></span>
15. <span data-ttu-id="38eeb-187">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="38eeb-188">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="38eeb-189">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-189">Click Bind.</span></span>
18. <span data-ttu-id="38eeb-190">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="38eeb-191">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="38eeb-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="38eeb-192">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-192">Click Bind.</span></span>
21. <span data-ttu-id="38eeb-193">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="38eeb-194">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="38eeb-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="38eeb-195">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-195">Click Bind.</span></span>
24. <span data-ttu-id="38eeb-196">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="38eeb-197">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="38eeb-198">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-198">Click Bind.</span></span>
27. <span data-ttu-id="38eeb-199">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="38eeb-200">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="38eeb-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="38eeb-201">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-201">Click Bind.</span></span>
30. <span data-ttu-id="38eeb-202">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="38eeb-203">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="38eeb-204">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-204">Click Bind.</span></span>
33. <span data-ttu-id="38eeb-205">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="38eeb-206">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="38eeb-207">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-207">Click Bind.</span></span>
36. <span data-ttu-id="38eeb-208">Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="38eeb-209">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="38eeb-210">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-210">Click Bind.</span></span>
39. <span data-ttu-id="38eeb-211">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="38eeb-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="38eeb-212">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="38eeb-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="38eeb-213">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-213">Click Bind.</span></span>
42. <span data-ttu-id="38eeb-214">Valitse puussa "Root: XML Element\Company: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="38eeb-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="38eeb-215">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="38eeb-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="38eeb-216">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="38eeb-216">Click Bind.</span></span>
45. <span data-ttu-id="38eeb-217">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="38eeb-217">Click Save.</span></span>
46. <span data-ttu-id="38eeb-218">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38eeb-218">Close the page.</span></span>
<span data-ttu-id="38eeb-219">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="38eeb-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]