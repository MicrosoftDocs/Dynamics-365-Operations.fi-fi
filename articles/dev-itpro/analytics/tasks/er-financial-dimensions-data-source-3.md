--- 
title: "Raporttien suunnitteleminen taloushallinnon dimensioiden käyttämiseksi tietolähteinä"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="26c39-103">Raporttien suunnitteleminen taloushallinnon dimensioiden käyttämiseksi tietolähteinä</span><span class="sxs-lookup"><span data-stu-id="26c39-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26c39-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.</span><span class="sxs-lookup"><span data-stu-id="26c39-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="26c39-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="26c39-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="26c39-106">Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.</span><span class="sxs-lookup"><span data-stu-id="26c39-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="26c39-107">Suunnittele raportti, jossa esitetään taloushallinnon dimensioita</span><span class="sxs-lookup"><span data-stu-id="26c39-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="26c39-108">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="26c39-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="26c39-109">Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".</span><span class="sxs-lookup"><span data-stu-id="26c39-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="26c39-110">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="26c39-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="26c39-111">Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.</span><span class="sxs-lookup"><span data-stu-id="26c39-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="26c39-112">Käytä etukäteen luotua mallia uuden raportin tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="26c39-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="26c39-113">Kirjoita Nimi-kenttään Kirjauskansioraportti.</span><span class="sxs-lookup"><span data-stu-id="26c39-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="26c39-114">Valitse Tietomallin määritelmä -kentässä Kirjaus.</span><span class="sxs-lookup"><span data-stu-id="26c39-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="26c39-115">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="26c39-115">Click Create configuration.</span></span>
8. <span data-ttu-id="26c39-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="26c39-116">Click Designer.</span></span>
9. <span data-ttu-id="26c39-117">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="26c39-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="26c39-118">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="26c39-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="26c39-119">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="26c39-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="26c39-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-120">Click OK.</span></span>
13. <span data-ttu-id="26c39-121">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="26c39-122">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="26c39-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="26c39-123">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="26c39-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="26c39-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-124">Click OK.</span></span>
17. <span data-ttu-id="26c39-125">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="26c39-126">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="26c39-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="26c39-127">Kirjoita Nimi-kenttään "Kirjauskansio".</span><span class="sxs-lookup"><span data-stu-id="26c39-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="26c39-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-128">Click OK.</span></span>
21. <span data-ttu-id="26c39-129">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="26c39-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="26c39-131">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="26c39-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="26c39-132">Kirjoita Nimi-kenttään "Erä".</span><span class="sxs-lookup"><span data-stu-id="26c39-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="26c39-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-133">Click OK.</span></span>
26. <span data-ttu-id="26c39-134">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="26c39-135">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="26c39-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="26c39-136">Kirjoita Nimi-kenttään "Tapahtuma".</span><span class="sxs-lookup"><span data-stu-id="26c39-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="26c39-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-137">Click OK.</span></span>
30. <span data-ttu-id="26c39-138">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="26c39-139">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="26c39-140">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="26c39-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="26c39-141">Kirjoita Nimi-kenttään "Tosite".</span><span class="sxs-lookup"><span data-stu-id="26c39-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="26c39-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-142">Click OK.</span></span>
35. <span data-ttu-id="26c39-143">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="26c39-144">Kirjoita Nimi-kenttään "Päivämäärä".</span><span class="sxs-lookup"><span data-stu-id="26c39-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="26c39-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-145">Click OK.</span></span>
38. <span data-ttu-id="26c39-146">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="26c39-147">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="26c39-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="26c39-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-148">Click OK.</span></span>
41. <span data-ttu-id="26c39-149">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="26c39-150">Kirjoita Nimi-kenttään "Dt".</span><span class="sxs-lookup"><span data-stu-id="26c39-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="26c39-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-151">Click OK.</span></span>
44. <span data-ttu-id="26c39-152">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="26c39-153">Kirjoita Nimi-kenttään "Ct".</span><span class="sxs-lookup"><span data-stu-id="26c39-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="26c39-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-154">Click OK.</span></span>
47. <span data-ttu-id="26c39-155">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="26c39-156">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="26c39-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="26c39-157">Kirjoita Nimi-kenttään "Dimensiot".</span><span class="sxs-lookup"><span data-stu-id="26c39-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="26c39-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-158">Click OK.</span></span>
51. <span data-ttu-id="26c39-159">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="26c39-160">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="26c39-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="26c39-161">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="26c39-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="26c39-162">Kirjoita Nimi-kenttään "Koodi".</span><span class="sxs-lookup"><span data-stu-id="26c39-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="26c39-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-163">Click OK.</span></span>
56. <span data-ttu-id="26c39-164">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="26c39-165">Kirjoita Nimi-kenttään "Arvo".</span><span class="sxs-lookup"><span data-stu-id="26c39-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="26c39-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-166">Click OK.</span></span>
59. <span data-ttu-id="26c39-167">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="26c39-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="26c39-168">Kirjoita Nimi-kenttään. "Kuv."</span><span class="sxs-lookup"><span data-stu-id="26c39-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="26c39-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="26c39-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="26c39-170">Yhdistä raportin osat tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="26c39-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="26c39-171">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="26c39-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="26c39-172">Laajenna puussa "model: Data model Financial dimensions sample model".</span><span class="sxs-lookup"><span data-stu-id="26c39-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="26c39-173">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="26c39-174">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="26c39-175">Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="26c39-176">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="26c39-177">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="26c39-178">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-178">Click Bind.</span></span>
9. <span data-ttu-id="26c39-179">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="26c39-180">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="26c39-181">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-181">Click Bind.</span></span>
12. <span data-ttu-id="26c39-182">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="26c39-183">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="26c39-184">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-184">Click Bind.</span></span>
15. <span data-ttu-id="26c39-185">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="26c39-186">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="26c39-187">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-187">Click Bind.</span></span>
18. <span data-ttu-id="26c39-188">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="26c39-189">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".</span><span class="sxs-lookup"><span data-stu-id="26c39-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="26c39-190">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-190">Click Bind.</span></span>
21. <span data-ttu-id="26c39-191">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="26c39-192">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".</span><span class="sxs-lookup"><span data-stu-id="26c39-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="26c39-193">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-193">Click Bind.</span></span>
24. <span data-ttu-id="26c39-194">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="26c39-195">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="26c39-196">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-196">Click Bind.</span></span>
27. <span data-ttu-id="26c39-197">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="26c39-198">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".</span><span class="sxs-lookup"><span data-stu-id="26c39-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="26c39-199">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-199">Click Bind.</span></span>
30. <span data-ttu-id="26c39-200">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="26c39-201">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="26c39-202">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-202">Click Bind.</span></span>
33. <span data-ttu-id="26c39-203">Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="26c39-204">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="26c39-205">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-205">Click Bind.</span></span>
36. <span data-ttu-id="26c39-206">Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="26c39-207">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="26c39-208">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-208">Click Bind.</span></span>
39. <span data-ttu-id="26c39-209">Valitse puussa "Root: XML Element\Journal: XML Element".</span><span class="sxs-lookup"><span data-stu-id="26c39-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="26c39-210">Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".</span><span class="sxs-lookup"><span data-stu-id="26c39-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="26c39-211">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-211">Click Bind.</span></span>
42. <span data-ttu-id="26c39-212">Valitse puussa "Root: XML Element\Company: XML Attribute".</span><span class="sxs-lookup"><span data-stu-id="26c39-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="26c39-213">Valitse puussa "model: Data model Financial dimensions sample model\Company: String".</span><span class="sxs-lookup"><span data-stu-id="26c39-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="26c39-214">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="26c39-214">Click Bind.</span></span>
45. <span data-ttu-id="26c39-215">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="26c39-215">Click Save.</span></span>
46. <span data-ttu-id="26c39-216">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="26c39-216">Close the page.</span></span>


