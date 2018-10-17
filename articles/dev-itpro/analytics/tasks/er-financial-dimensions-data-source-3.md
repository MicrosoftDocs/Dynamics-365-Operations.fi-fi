--- 
title: "ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 45096a728ad6f9e331b53b4e12ca0ff9317a3939
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="54caf-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 3: raportin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="54caf-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54caf-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="54caf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="54caf-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="54caf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="54caf-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="54caf-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="54caf-107">Suunnittele raportti, jossa esitetään taloushallinnon dimensioita</span><span class="sxs-lookup"><span data-stu-id="54caf-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="54caf-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="54caf-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="54caf-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="54caf-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="54caf-110">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="54caf-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="54caf-111">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="54caf-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="54caf-112">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="54caf-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="54caf-113">Kirjoita Nimi-kenttään Kirjauskansioraportti.</span><span class="sxs-lookup"><span data-stu-id="54caf-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="54caf-114">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="54caf-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="54caf-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="54caf-115">Click Create configuration.</span></span>
8. <span data-ttu-id="54caf-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="54caf-116">Click Designer.</span></span>
9. <span data-ttu-id="54caf-117">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="54caf-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="54caf-118">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="54caf-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="54caf-119">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="54caf-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="54caf-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-120">Click OK.</span></span>
13. <span data-ttu-id="54caf-121">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="54caf-122">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="54caf-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="54caf-123">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="54caf-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="54caf-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-124">Click OK.</span></span>
17. <span data-ttu-id="54caf-125">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="54caf-126">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="54caf-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="54caf-127">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="54caf-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="54caf-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-128">Click OK.</span></span>
21. <span data-ttu-id="54caf-129">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="54caf-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="54caf-131">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="54caf-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="54caf-132">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="54caf-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="54caf-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-133">Click OK.</span></span>
26. <span data-ttu-id="54caf-134">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="54caf-135">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="54caf-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="54caf-136">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="54caf-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="54caf-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-137">Click OK.</span></span>
30. <span data-ttu-id="54caf-138">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="54caf-139">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="54caf-140">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="54caf-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="54caf-141">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="54caf-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="54caf-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-142">Click OK.</span></span>
35. <span data-ttu-id="54caf-143">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="54caf-144">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="54caf-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="54caf-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-145">Click OK.</span></span>
38. <span data-ttu-id="54caf-146">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="54caf-147">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="54caf-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="54caf-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-148">Click OK.</span></span>
41. <span data-ttu-id="54caf-149">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="54caf-150">Kirjoita Nimi-kenttään "Dt".</span><span class="sxs-lookup"><span data-stu-id="54caf-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="54caf-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-151">Click OK.</span></span>
44. <span data-ttu-id="54caf-152">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="54caf-153">Kirjoita Nimi-kenttään "Ct".</span><span class="sxs-lookup"><span data-stu-id="54caf-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="54caf-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-154">Click OK.</span></span>
47. <span data-ttu-id="54caf-155">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="54caf-156">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="54caf-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="54caf-157">Kirjoita Nimi-kenttään "Dimensiot".</span><span class="sxs-lookup"><span data-stu-id="54caf-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="54caf-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-158">Click OK.</span></span>
51. <span data-ttu-id="54caf-159">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="54caf-160">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="54caf-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="54caf-161">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="54caf-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="54caf-162">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="54caf-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="54caf-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-163">Click OK.</span></span>
56. <span data-ttu-id="54caf-164">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="54caf-165">Kirjoita Nimi-kenttään "Arvo".</span><span class="sxs-lookup"><span data-stu-id="54caf-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="54caf-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-166">Click OK.</span></span>
59. <span data-ttu-id="54caf-167">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="54caf-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="54caf-168">Kirjoita Nimi-kenttään. "Kuv."</span><span class="sxs-lookup"><span data-stu-id="54caf-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="54caf-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54caf-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="54caf-170">Yhdistä raportin osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="54caf-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="54caf-171">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="54caf-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="54caf-172">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="54caf-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="54caf-173">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="54caf-174">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="54caf-175">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="54caf-176">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="54caf-177">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="54caf-178">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-178">Click Bind.</span></span>
9. <span data-ttu-id="54caf-179">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="54caf-180">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="54caf-181">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-181">Click Bind.</span></span>
12. <span data-ttu-id="54caf-182">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="54caf-183">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="54caf-184">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-184">Click Bind.</span></span>
15. <span data-ttu-id="54caf-185">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="54caf-186">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="54caf-187">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-187">Click Bind.</span></span>
18. <span data-ttu-id="54caf-188">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="54caf-189">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="54caf-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="54caf-190">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-190">Click Bind.</span></span>
21. <span data-ttu-id="54caf-191">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="54caf-192">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="54caf-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="54caf-193">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-193">Click Bind.</span></span>
24. <span data-ttu-id="54caf-194">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="54caf-195">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="54caf-196">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-196">Click Bind.</span></span>
27. <span data-ttu-id="54caf-197">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="54caf-198">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="54caf-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="54caf-199">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-199">Click Bind.</span></span>
30. <span data-ttu-id="54caf-200">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="54caf-201">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="54caf-202">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-202">Click Bind.</span></span>
33. <span data-ttu-id="54caf-203">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="54caf-204">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="54caf-205">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-205">Click Bind.</span></span>
36. <span data-ttu-id="54caf-206">Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="54caf-207">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="54caf-208">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-208">Click Bind.</span></span>
39. <span data-ttu-id="54caf-209">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="54caf-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="54caf-210">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="54caf-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="54caf-211">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-211">Click Bind.</span></span>
42. <span data-ttu-id="54caf-212">Valitse puussa "Root: XML Element\Company: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="54caf-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="54caf-213">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="54caf-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="54caf-214">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="54caf-214">Click Bind.</span></span>
45. <span data-ttu-id="54caf-215">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="54caf-215">Click Save.</span></span>
46. <span data-ttu-id="54caf-216">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54caf-216">Close the page.</span></span>


