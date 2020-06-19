---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cef61787e50561eaac4fd52741ab5f90d9c4171d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406494"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="70206-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="70206-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70206-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="70206-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="70206-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="70206-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="70206-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="70206-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="70206-107">Suunnittele raportti, jossa esitetään taloushallinnon dimensioita</span><span class="sxs-lookup"><span data-stu-id="70206-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="70206-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="70206-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="70206-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="70206-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="70206-110">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="70206-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="70206-111">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="70206-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="70206-112">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="70206-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="70206-113">Kirjoita Nimi-kenttään Kirjauskansioraportti.</span><span class="sxs-lookup"><span data-stu-id="70206-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="70206-114">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="70206-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="70206-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="70206-115">Click Create configuration.</span></span>
8. <span data-ttu-id="70206-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="70206-116">Click Designer.</span></span>
9. <span data-ttu-id="70206-117">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="70206-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="70206-118">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="70206-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="70206-119">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="70206-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="70206-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-120">Click OK.</span></span>
13. <span data-ttu-id="70206-121">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="70206-122">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="70206-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="70206-123">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="70206-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="70206-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-124">Click OK.</span></span>
17. <span data-ttu-id="70206-125">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="70206-126">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="70206-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="70206-127">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="70206-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="70206-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-128">Click OK.</span></span>
21. <span data-ttu-id="70206-129">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="70206-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="70206-131">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="70206-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="70206-132">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="70206-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="70206-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-133">Click OK.</span></span>
26. <span data-ttu-id="70206-134">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="70206-135">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="70206-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="70206-136">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="70206-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="70206-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-137">Click OK.</span></span>
30. <span data-ttu-id="70206-138">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="70206-139">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="70206-140">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="70206-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="70206-141">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="70206-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="70206-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-142">Click OK.</span></span>
35. <span data-ttu-id="70206-143">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="70206-144">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="70206-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="70206-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-145">Click OK.</span></span>
38. <span data-ttu-id="70206-146">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="70206-147">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="70206-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="70206-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-148">Click OK.</span></span>
41. <span data-ttu-id="70206-149">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="70206-150">Kirjoita Nimi-kenttään "Dt".</span><span class="sxs-lookup"><span data-stu-id="70206-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="70206-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-151">Click OK.</span></span>
44. <span data-ttu-id="70206-152">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="70206-153">Kirjoita Nimi-kenttään "Ct".</span><span class="sxs-lookup"><span data-stu-id="70206-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="70206-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-154">Click OK.</span></span>
47. <span data-ttu-id="70206-155">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="70206-156">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="70206-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="70206-157">Kirjoita Nimi-kenttään "Dimensiot".</span><span class="sxs-lookup"><span data-stu-id="70206-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="70206-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-158">Click OK.</span></span>
51. <span data-ttu-id="70206-159">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="70206-160">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="70206-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="70206-161">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="70206-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="70206-162">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="70206-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="70206-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-163">Click OK.</span></span>
56. <span data-ttu-id="70206-164">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="70206-165">Kirjoita Nimi-kenttään "Arvo".</span><span class="sxs-lookup"><span data-stu-id="70206-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="70206-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-166">Click OK.</span></span>
59. <span data-ttu-id="70206-167">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="70206-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="70206-168">Kirjoita Nimi-kenttään. "Kuv."</span><span class="sxs-lookup"><span data-stu-id="70206-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="70206-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70206-169">Click OK.</span></span>
<span data-ttu-id="70206-170">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="70206-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="70206-171">Yhdistä raportin osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="70206-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="70206-172">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="70206-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="70206-173">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="70206-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="70206-174">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="70206-175">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="70206-176">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="70206-177">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="70206-178">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".</span><span class="sxs-lookup"><span data-stu-id="70206-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="70206-179">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-179">Click Bind.</span></span>
9. <span data-ttu-id="70206-180">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="70206-181">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="70206-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="70206-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-182">Click Bind.</span></span>
12. <span data-ttu-id="70206-183">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="70206-184">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".</span><span class="sxs-lookup"><span data-stu-id="70206-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="70206-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-185">Click Bind.</span></span>
15. <span data-ttu-id="70206-186">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="70206-187">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="70206-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-188">Click Bind.</span></span>
18. <span data-ttu-id="70206-189">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="70206-190">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="70206-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="70206-191">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-191">Click Bind.</span></span>
21. <span data-ttu-id="70206-192">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="70206-193">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="70206-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="70206-194">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-194">Click Bind.</span></span>
24. <span data-ttu-id="70206-195">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="70206-196">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="70206-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="70206-197">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-197">Click Bind.</span></span>
27. <span data-ttu-id="70206-198">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="70206-199">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="70206-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="70206-200">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-200">Click Bind.</span></span>
30. <span data-ttu-id="70206-201">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="70206-202">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="70206-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="70206-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-203">Click Bind.</span></span>
33. <span data-ttu-id="70206-204">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="70206-205">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="70206-206">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-206">Click Bind.</span></span>
36. <span data-ttu-id="70206-207">Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="70206-208">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="70206-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="70206-209">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-209">Click Bind.</span></span>
39. <span data-ttu-id="70206-210">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="70206-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="70206-211">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="70206-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="70206-212">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-212">Click Bind.</span></span>
42. <span data-ttu-id="70206-213">Valitse puussa "Root: XML Element\Company: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="70206-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="70206-214">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="70206-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="70206-215">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="70206-215">Click Bind.</span></span>
45. <span data-ttu-id="70206-216">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="70206-216">Click Save.</span></span>
46. <span data-ttu-id="70206-217">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="70206-217">Close the page.</span></span>
<span data-ttu-id="70206-218">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="70206-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

