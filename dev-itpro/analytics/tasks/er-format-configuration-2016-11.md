--- 
title: "Muotokonfiguraation luominen sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="92f7d-103">Muotokonfiguraation luominen sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="92f7d-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92f7d-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda muotokonfiguraation sähköiselle raportoinnille (ER).</span><span class="sxs-lookup"><span data-stu-id="92f7d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="92f7d-105">Tämä muotokonfiguraatio määrittää maksujen käsittelyssä käytettävien sähköisten asiakirjojen muodon.</span><span class="sxs-lookup"><span data-stu-id="92f7d-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="92f7d-106">Tässä esimerkissä luodaan muotokonfiguraatio Litware, Inc. -malliyritykselle. Voit suorittaa nämä vaiheet suoritettuasi ensin Mallin yhdistäminen valittuihin tietolähteisiin -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="92f7d-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="92f7d-107">Uuden muotokonfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="92f7d-107">Create a new format configuration</span></span>
1. <span data-ttu-id="92f7d-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="92f7d-109">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="92f7d-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="92f7d-110">Valitse puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="92f7d-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="92f7d-111">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="92f7d-112">Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="92f7d-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="92f7d-113">Syötä Nimi-kenttään BACS (Iso-Britannia, kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="92f7d-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="92f7d-114">BACS (Iso-Britannia, kuvitteellinen)</span><span class="sxs-lookup"><span data-stu-id="92f7d-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="92f7d-115">Syötä kuvaus-kenttään BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="92f7d-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="92f7d-116">BACS - toimittajan maksumuoto (Iso-Britannia, kuvitteellinen)</span><span class="sxs-lookup"><span data-stu-id="92f7d-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="92f7d-117">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="92f7d-118">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="92f7d-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="92f7d-119">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="92f7d-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="92f7d-120">Voit määrittää sähköiselle asiakirjalle tietyn muodon.</span><span class="sxs-lookup"><span data-stu-id="92f7d-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="92f7d-121">Jätä kenttä tyhjäksi, jos haluat valita muodon suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="92f7d-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="92f7d-122">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="92f7d-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="92f7d-123">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="92f7d-123">Click Create configuration.</span></span>
    * <span data-ttu-id="92f7d-124">Uusi konfiguraatio on luotu.</span><span class="sxs-lookup"><span data-stu-id="92f7d-124">A new configuration has been created.</span></span> <span data-ttu-id="92f7d-125">Rakenteen muodon voi tallentaa luonnoksena sähköisten asiakirjojen hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="92f7d-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="92f7d-126">Sähköisen asiakirjan muodon suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="92f7d-126">Design format of electronic document</span></span>
1. <span data-ttu-id="92f7d-127">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="92f7d-127">Click Designer.</span></span>
2. <span data-ttu-id="92f7d-128">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="92f7d-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="92f7d-129">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="92f7d-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="92f7d-130">Syötä Nimi-kenttään Xml.</span><span class="sxs-lookup"><span data-stu-id="92f7d-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="92f7d-131">XML</span><span class="sxs-lookup"><span data-stu-id="92f7d-131">Xml</span></span>  
5. <span data-ttu-id="92f7d-132">Syötä Koodaus-kenttään UTF-8.</span><span class="sxs-lookup"><span data-stu-id="92f7d-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="92f7d-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="92f7d-133">UTF-8</span></span>  
6. <span data-ttu-id="92f7d-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-134">Click OK.</span></span>
7. <span data-ttu-id="92f7d-135">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="92f7d-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="92f7d-136">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="92f7d-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="92f7d-137">Syötä Nimi-kenttään Viesti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="92f7d-138">Viesti</span><span class="sxs-lookup"><span data-stu-id="92f7d-138">Message</span></span>  
10. <span data-ttu-id="92f7d-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-139">Click OK.</span></span>
11. <span data-ttu-id="92f7d-140">Valitse puussa Xml\Sanoma.</span><span class="sxs-lookup"><span data-stu-id="92f7d-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="92f7d-141">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-141">Click Add Element.</span></span>
13. <span data-ttu-id="92f7d-142">Syötä Nimi-kenttään ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="92f7d-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="92f7d-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="92f7d-143">ProcessingDate</span></span>  
14. <span data-ttu-id="92f7d-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-144">Click OK.</span></span>
15. <span data-ttu-id="92f7d-145">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-145">Click Add Element.</span></span>
16. <span data-ttu-id="92f7d-146">Syötä Nimi-kenttään MessageId.</span><span class="sxs-lookup"><span data-stu-id="92f7d-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="92f7d-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="92f7d-147">MessageId</span></span>  
17. <span data-ttu-id="92f7d-148">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-148">Click OK.</span></span>
18. <span data-ttu-id="92f7d-149">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-149">Click Add Element.</span></span>
19. <span data-ttu-id="92f7d-150">Syötä Nimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="92f7d-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="92f7d-151">Maksut</span><span class="sxs-lookup"><span data-stu-id="92f7d-151">Payments</span></span>  
20. <span data-ttu-id="92f7d-152">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-152">Click OK.</span></span>
21. <span data-ttu-id="92f7d-153">Valitse puussa Xml\Sanoma\Maksut.</span><span class="sxs-lookup"><span data-stu-id="92f7d-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="92f7d-154">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-154">Click Add Element.</span></span>
23. <span data-ttu-id="92f7d-155">Syötä Nimi-kenttään Nimike.</span><span class="sxs-lookup"><span data-stu-id="92f7d-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="92f7d-156">Nimike</span><span class="sxs-lookup"><span data-stu-id="92f7d-156">Item</span></span>  
24. <span data-ttu-id="92f7d-157">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-157">Click OK.</span></span>
25. <span data-ttu-id="92f7d-158">Valitse puussa Xml\Sanoma\Maksut\Nimike.</span><span class="sxs-lookup"><span data-stu-id="92f7d-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="92f7d-159">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="92f7d-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="92f7d-160">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="92f7d-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="92f7d-161">Syötä Nimi-kenttään Tunnus.</span><span class="sxs-lookup"><span data-stu-id="92f7d-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="92f7d-162">Tunnus</span><span class="sxs-lookup"><span data-stu-id="92f7d-162">Id</span></span>  
29. <span data-ttu-id="92f7d-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-163">Click OK.</span></span>
30. <span data-ttu-id="92f7d-164">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="92f7d-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="92f7d-165">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="92f7d-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="92f7d-166">Syötä Nimi-kenttään Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="92f7d-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="92f7d-167">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="92f7d-167">Vendor</span></span>  
33. <span data-ttu-id="92f7d-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-168">Click OK.</span></span>
34. <span data-ttu-id="92f7d-169">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="92f7d-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="92f7d-170">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-170">Click Add Element.</span></span>
36. <span data-ttu-id="92f7d-171">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="92f7d-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="92f7d-172">Name</span></span>  
37. <span data-ttu-id="92f7d-173">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-173">Click OK.</span></span>
38. <span data-ttu-id="92f7d-174">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-174">Click Add Element.</span></span>
39. <span data-ttu-id="92f7d-175">Syötä Nimi-kenttään Pankki.</span><span class="sxs-lookup"><span data-stu-id="92f7d-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="92f7d-176">Pankki</span><span class="sxs-lookup"><span data-stu-id="92f7d-176">Bank</span></span>  
40. <span data-ttu-id="92f7d-177">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-177">Click OK.</span></span>
41. <span data-ttu-id="92f7d-178">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki.</span><span class="sxs-lookup"><span data-stu-id="92f7d-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="92f7d-179">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-179">Click Add Element.</span></span>
43. <span data-ttu-id="92f7d-180">Syötä Nimi-kenttään RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="92f7d-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="92f7d-181">RoutingNumber</span></span>  
44. <span data-ttu-id="92f7d-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-182">Click OK.</span></span>
45. <span data-ttu-id="92f7d-183">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-183">Click Add Element.</span></span>
46. <span data-ttu-id="92f7d-184">Syötä Nimi-kenttään AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="92f7d-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="92f7d-185">AccountNumber</span></span>  
47. <span data-ttu-id="92f7d-186">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-186">Click OK.</span></span>
48. <span data-ttu-id="92f7d-187">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="92f7d-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="92f7d-188">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-188">Click Copy.</span></span>
50. <span data-ttu-id="92f7d-189">Valitse puussa Xml\Sanoma\Maksut\Nimike.</span><span class="sxs-lookup"><span data-stu-id="92f7d-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="92f7d-190">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="92f7d-190">Click Paste.</span></span>
52. <span data-ttu-id="92f7d-191">Syötä Nimi-kenttään Maksaja.</span><span class="sxs-lookup"><span data-stu-id="92f7d-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="92f7d-192">Maksaja</span><span class="sxs-lookup"><span data-stu-id="92f7d-192">Payer</span></span>  
53. <span data-ttu-id="92f7d-193">Valitse puussa Xml\Sanoma\Maksut\Nimike.</span><span class="sxs-lookup"><span data-stu-id="92f7d-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="92f7d-194">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-194">Click Add Element.</span></span>
55. <span data-ttu-id="92f7d-195">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="92f7d-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="92f7d-196">Valuutta</span><span class="sxs-lookup"><span data-stu-id="92f7d-196">Currency</span></span>  
56. <span data-ttu-id="92f7d-197">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-197">Click OK.</span></span>
57. <span data-ttu-id="92f7d-198">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-198">Click Add Element.</span></span>
58. <span data-ttu-id="92f7d-199">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="92f7d-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="92f7d-200">kuvaus</span><span class="sxs-lookup"><span data-stu-id="92f7d-200">Description</span></span>  
59. <span data-ttu-id="92f7d-201">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-201">Click OK.</span></span>
60. <span data-ttu-id="92f7d-202">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-202">Click Add Element.</span></span>
61. <span data-ttu-id="92f7d-203">Syötä Nimi-kenttään TransDate.</span><span class="sxs-lookup"><span data-stu-id="92f7d-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="92f7d-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="92f7d-204">TransDate</span></span>  
62. <span data-ttu-id="92f7d-205">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-205">Click OK.</span></span>
63. <span data-ttu-id="92f7d-206">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="92f7d-206">Click Add Element.</span></span>
64. <span data-ttu-id="92f7d-207">Syötä Nimi-kenttään Summa.</span><span class="sxs-lookup"><span data-stu-id="92f7d-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="92f7d-208">Määrä</span><span class="sxs-lookup"><span data-stu-id="92f7d-208">Amount</span></span>  
65. <span data-ttu-id="92f7d-209">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="92f7d-210">Muotokomponenttien valmisteleminen tietomallielementtien yhdistämistä varten</span><span class="sxs-lookup"><span data-stu-id="92f7d-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="92f7d-211">Valitse puussa Xml\Sanoma\ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="92f7d-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="92f7d-212">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="92f7d-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="92f7d-213">Valitse puussa Teksti\DateTime.</span><span class="sxs-lookup"><span data-stu-id="92f7d-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="92f7d-214">Syötä Muoto-kenttään vvvv-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="92f7d-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="92f7d-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="92f7d-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="92f7d-216">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-216">Click OK.</span></span>
6. <span data-ttu-id="92f7d-217">Valitse puussa Xml\Sanoma\Maksut\Nimike\TransDate.</span><span class="sxs-lookup"><span data-stu-id="92f7d-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="92f7d-218">Valitse Lisää DateTime.</span><span class="sxs-lookup"><span data-stu-id="92f7d-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="92f7d-219">Syötä Muoto-kenttään vvvv-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="92f7d-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="92f7d-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="92f7d-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="92f7d-221">Valitse DateTime-tyyppi-kentässä Date.</span><span class="sxs-lookup"><span data-stu-id="92f7d-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="92f7d-222">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-222">Click OK.</span></span>
11. <span data-ttu-id="92f7d-223">Valitse puussa Xml\Sanoma\MessageId.</span><span class="sxs-lookup"><span data-stu-id="92f7d-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="92f7d-224">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="92f7d-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="92f7d-225">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="92f7d-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="92f7d-226">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-226">Click OK.</span></span>
15. <span data-ttu-id="92f7d-227">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="92f7d-228">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-228">Click Add String.</span></span>
17. <span data-ttu-id="92f7d-229">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-229">Click OK.</span></span>
18. <span data-ttu-id="92f7d-230">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="92f7d-231">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-231">Click Add String.</span></span>
20. <span data-ttu-id="92f7d-232">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-232">Click OK.</span></span>
21. <span data-ttu-id="92f7d-233">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="92f7d-234">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-234">Click Add String.</span></span>
23. <span data-ttu-id="92f7d-235">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-235">Click OK.</span></span>
24. <span data-ttu-id="92f7d-236">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi.</span><span class="sxs-lookup"><span data-stu-id="92f7d-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="92f7d-237">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-237">Click Add String.</span></span>
26. <span data-ttu-id="92f7d-238">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-238">Click OK.</span></span>
27. <span data-ttu-id="92f7d-239">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="92f7d-240">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-240">Click Add String.</span></span>
29. <span data-ttu-id="92f7d-241">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-241">Click OK.</span></span>
30. <span data-ttu-id="92f7d-242">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="92f7d-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="92f7d-243">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-243">Click Add String.</span></span>
32. <span data-ttu-id="92f7d-244">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-244">Click OK.</span></span>
33. <span data-ttu-id="92f7d-245">Valitse puussa Xml\Sanoma\Maksut\Nimike\Valuutta.</span><span class="sxs-lookup"><span data-stu-id="92f7d-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="92f7d-246">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-246">Click Add String.</span></span>
35. <span data-ttu-id="92f7d-247">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-247">Click OK.</span></span>
36. <span data-ttu-id="92f7d-248">Valitse puussa Xml\Sanoma\Maksut\Nimike\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="92f7d-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="92f7d-249">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-249">Click Add String.</span></span>
38. <span data-ttu-id="92f7d-250">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-250">Click OK.</span></span>
39. <span data-ttu-id="92f7d-251">Valitse puussa Xml\Sanoma\Maksut\Nimike\Summa.</span><span class="sxs-lookup"><span data-stu-id="92f7d-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="92f7d-252">Valitse Lisää merkkijono.</span><span class="sxs-lookup"><span data-stu-id="92f7d-252">Click Add String.</span></span>
41. <span data-ttu-id="92f7d-253">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="92f7d-253">Click OK.</span></span>
42. <span data-ttu-id="92f7d-254">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="92f7d-254">Click Save.</span></span>
43. <span data-ttu-id="92f7d-255">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="92f7d-255">Close the page.</span></span>


