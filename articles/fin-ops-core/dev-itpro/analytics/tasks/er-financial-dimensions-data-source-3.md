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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684784"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="7ec45-103">ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)</span><span class="sxs-lookup"><span data-stu-id="7ec45-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ec45-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="7ec45-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="7ec45-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="7ec45-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7ec45-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="7ec45-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="7ec45-107">Suunnittele raportti, jossa esitetään taloushallinnon dimensioita</span><span class="sxs-lookup"><span data-stu-id="7ec45-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="7ec45-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="7ec45-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7ec45-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="7ec45-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7ec45-110">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="7ec45-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="7ec45-111">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="7ec45-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="7ec45-112">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="7ec45-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="7ec45-113">Kirjoita Nimi-kenttään Kirjauskansioraportti.</span><span class="sxs-lookup"><span data-stu-id="7ec45-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="7ec45-114">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="7ec45-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="7ec45-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="7ec45-115">Click Create configuration.</span></span>
8. <span data-ttu-id="7ec45-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="7ec45-116">Click Designer.</span></span>
9. <span data-ttu-id="7ec45-117">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="7ec45-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="7ec45-118">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7ec45-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="7ec45-119">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="7ec45-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="7ec45-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-120">Click OK.</span></span>
13. <span data-ttu-id="7ec45-121">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="7ec45-122">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7ec45-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="7ec45-123">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="7ec45-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="7ec45-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-124">Click OK.</span></span>
17. <span data-ttu-id="7ec45-125">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="7ec45-126">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7ec45-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="7ec45-127">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="7ec45-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="7ec45-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-128">Click OK.</span></span>
21. <span data-ttu-id="7ec45-129">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="7ec45-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="7ec45-131">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7ec45-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="7ec45-132">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="7ec45-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="7ec45-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-133">Click OK.</span></span>
26. <span data-ttu-id="7ec45-134">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="7ec45-135">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7ec45-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="7ec45-136">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="7ec45-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="7ec45-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-137">Click OK.</span></span>
30. <span data-ttu-id="7ec45-138">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="7ec45-139">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="7ec45-140">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7ec45-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="7ec45-141">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="7ec45-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="7ec45-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-142">Click OK.</span></span>
35. <span data-ttu-id="7ec45-143">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="7ec45-144">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="7ec45-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="7ec45-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-145">Click OK.</span></span>
38. <span data-ttu-id="7ec45-146">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="7ec45-147">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="7ec45-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="7ec45-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-148">Click OK.</span></span>
41. <span data-ttu-id="7ec45-149">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="7ec45-150">Kirjoita Nimi-kenttään "Dt".</span><span class="sxs-lookup"><span data-stu-id="7ec45-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="7ec45-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-151">Click OK.</span></span>
44. <span data-ttu-id="7ec45-152">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="7ec45-153">Kirjoita Nimi-kenttään "Ct".</span><span class="sxs-lookup"><span data-stu-id="7ec45-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="7ec45-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-154">Click OK.</span></span>
47. <span data-ttu-id="7ec45-155">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="7ec45-156">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7ec45-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="7ec45-157">Kirjoita Nimi-kenttään "Dimensiot".</span><span class="sxs-lookup"><span data-stu-id="7ec45-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="7ec45-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-158">Click OK.</span></span>
51. <span data-ttu-id="7ec45-159">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="7ec45-160">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="7ec45-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="7ec45-161">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7ec45-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="7ec45-162">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="7ec45-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="7ec45-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-163">Click OK.</span></span>
56. <span data-ttu-id="7ec45-164">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="7ec45-165">Kirjoita Nimi-kenttään "Arvo".</span><span class="sxs-lookup"><span data-stu-id="7ec45-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="7ec45-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-166">Click OK.</span></span>
59. <span data-ttu-id="7ec45-167">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="7ec45-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="7ec45-168">Kirjoita Nimi-kenttään. "Kuv."</span><span class="sxs-lookup"><span data-stu-id="7ec45-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="7ec45-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7ec45-169">Click OK.</span></span>
<span data-ttu-id="7ec45-170">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="7ec45-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="7ec45-171">Yhdistä raportin osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="7ec45-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="7ec45-172">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7ec45-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="7ec45-173">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="7ec45-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7ec45-174">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="7ec45-175">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="7ec45-176">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="7ec45-177">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="7ec45-178">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="7ec45-179">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-179">Click Bind.</span></span>
9. <span data-ttu-id="7ec45-180">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="7ec45-181">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="7ec45-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-182">Click Bind.</span></span>
12. <span data-ttu-id="7ec45-183">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="7ec45-184">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="7ec45-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-185">Click Bind.</span></span>
15. <span data-ttu-id="7ec45-186">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="7ec45-187">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="7ec45-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-188">Click Bind.</span></span>
18. <span data-ttu-id="7ec45-189">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="7ec45-190">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="7ec45-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="7ec45-191">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-191">Click Bind.</span></span>
21. <span data-ttu-id="7ec45-192">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="7ec45-193">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="7ec45-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="7ec45-194">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-194">Click Bind.</span></span>
24. <span data-ttu-id="7ec45-195">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="7ec45-196">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="7ec45-197">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-197">Click Bind.</span></span>
27. <span data-ttu-id="7ec45-198">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="7ec45-199">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="7ec45-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="7ec45-200">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-200">Click Bind.</span></span>
30. <span data-ttu-id="7ec45-201">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="7ec45-202">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="7ec45-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-203">Click Bind.</span></span>
33. <span data-ttu-id="7ec45-204">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="7ec45-205">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="7ec45-206">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-206">Click Bind.</span></span>
36. <span data-ttu-id="7ec45-207">Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="7ec45-208">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="7ec45-209">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-209">Click Bind.</span></span>
39. <span data-ttu-id="7ec45-210">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="7ec45-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="7ec45-211">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="7ec45-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="7ec45-212">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-212">Click Bind.</span></span>
42. <span data-ttu-id="7ec45-213">Valitse puussa "Root: XML Element\Company: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="7ec45-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="7ec45-214">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="7ec45-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="7ec45-215">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="7ec45-215">Click Bind.</span></span>
45. <span data-ttu-id="7ec45-216">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7ec45-216">Click Save.</span></span>
46. <span data-ttu-id="7ec45-217">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ec45-217">Close the page.</span></span>
<span data-ttu-id="7ec45-218">![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="7ec45-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

