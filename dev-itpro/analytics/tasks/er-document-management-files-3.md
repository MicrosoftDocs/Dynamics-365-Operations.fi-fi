--- 
title: "Muodon luominen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5548839c4d394d45cfb39da50ca78dab4b4e08e4
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="9510c-103">Muodon luominen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="9510c-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9510c-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="9510c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9510c-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="9510c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9510c-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 2: laajenna tietomallia)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="9510c-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="9510c-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="9510c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="9510c-108">Uuden muodon luonti laskujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="9510c-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="9510c-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="9510c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9510c-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="9510c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9510c-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="9510c-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="9510c-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="9510c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="9510c-113">Luot muodon, jolla luodaan sähköisiä viestejä tiedostoista, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="9510c-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="9510c-114">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="9510c-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="9510c-115">Syötä Uusi-kenttään Muoto perustuu tietomalliin Myyntilaskumalli (mukautettu).</span><span class="sxs-lookup"><span data-stu-id="9510c-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="9510c-116">Kirjoita Nimi-kenttään "Sähköisen laskun malliviesti".</span><span class="sxs-lookup"><span data-stu-id="9510c-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="9510c-117">Sähköisen laskun esimerkkisanoma</span><span class="sxs-lookup"><span data-stu-id="9510c-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="9510c-118">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="9510c-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="9510c-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="9510c-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="9510c-120">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="9510c-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="9510c-121">Muodon suunnittelu, joka täyttää liitteet viestiin MIME-muodossa</span><span class="sxs-lookup"><span data-stu-id="9510c-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="9510c-122">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="9510c-122">Click Designer.</span></span>
2. <span data-ttu-id="9510c-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="9510c-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="9510c-124">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="9510c-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="9510c-125">Kirjoita Nimi-kenttään "Lasku".</span><span class="sxs-lookup"><span data-stu-id="9510c-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="9510c-126">Lasku</span><span class="sxs-lookup"><span data-stu-id="9510c-126">Invoice</span></span>  
5. <span data-ttu-id="9510c-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-127">Click OK.</span></span>
6. <span data-ttu-id="9510c-128">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9510c-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="9510c-129">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="9510c-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="9510c-130">Syötä Nimi-kenttään "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="9510c-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="9510c-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="9510c-131">SalesOrder</span></span>  
9. <span data-ttu-id="9510c-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-132">Click OK.</span></span>
10. <span data-ttu-id="9510c-133">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="9510c-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="9510c-134">Syötä Nimi-kenttään "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="9510c-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="9510c-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="9510c-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="9510c-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-136">Click OK.</span></span>
13. <span data-ttu-id="9510c-137">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="9510c-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="9510c-138">Kirjoita Nimi-kenttään "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="9510c-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="9510c-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="9510c-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="9510c-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-140">Click OK.</span></span>
16. <span data-ttu-id="9510c-141">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9510c-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="9510c-142">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="9510c-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="9510c-143">Kirjoita Nimi-kenttään "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="9510c-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="9510c-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="9510c-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="9510c-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-145">Click OK.</span></span>
20. <span data-ttu-id="9510c-146">Valitse puusta 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="9510c-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="9510c-147">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="9510c-147">Click Add Element.</span></span>
22. <span data-ttu-id="9510c-148">Kirjoita Nimi-kenttään "Document".</span><span class="sxs-lookup"><span data-stu-id="9510c-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="9510c-149">Asiakirja</span><span class="sxs-lookup"><span data-stu-id="9510c-149">Document</span></span>  
23. <span data-ttu-id="9510c-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-150">Click OK.</span></span>
24. <span data-ttu-id="9510c-151">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="9510c-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="9510c-152">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9510c-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="9510c-153">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="9510c-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="9510c-154">Kirjoita Nimi-kenttään "FileName".</span><span class="sxs-lookup"><span data-stu-id="9510c-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="9510c-155">FileName</span><span class="sxs-lookup"><span data-stu-id="9510c-155">FileName</span></span>  
28. <span data-ttu-id="9510c-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-156">Click OK.</span></span>
29. <span data-ttu-id="9510c-157">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9510c-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="9510c-158">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="9510c-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="9510c-159">Kirjoita Nimi-kenttään "FileContent".</span><span class="sxs-lookup"><span data-stu-id="9510c-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="9510c-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="9510c-160">FileContent</span></span>  
32. <span data-ttu-id="9510c-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-161">Click OK.</span></span>
33. <span data-ttu-id="9510c-162">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent".</span><span class="sxs-lookup"><span data-stu-id="9510c-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="9510c-163">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="9510c-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="9510c-164">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="9510c-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="9510c-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9510c-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="9510c-166">Yhdistä muodon elementit tietomalliin tietolähteenä</span><span class="sxs-lookup"><span data-stu-id="9510c-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="9510c-167">Valitse puusta "Invoice\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="9510c-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="9510c-168">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9510c-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="9510c-169">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="9510c-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="9510c-170">Valitse puussa "model\Sales order number(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="9510c-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="9510c-171">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-171">Click Bind.</span></span>
6. <span data-ttu-id="9510c-172">Valitse puusta "Invoice\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="9510c-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="9510c-173">Laajenna puussa "model\Base invoice(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="9510c-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="9510c-174">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice number(Id)".</span><span class="sxs-lookup"><span data-stu-id="9510c-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="9510c-175">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-175">Click Bind.</span></span>
10. <span data-ttu-id="9510c-176">Valitse puusta "Invoice\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="9510c-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="9510c-177">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice amount(Amount)".</span><span class="sxs-lookup"><span data-stu-id="9510c-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="9510c-178">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-178">Click Bind.</span></span>
13. <span data-ttu-id="9510c-179">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="9510c-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="9510c-180">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="9510c-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="9510c-181">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="9510c-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="9510c-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-182">Click Bind.</span></span>
17. <span data-ttu-id="9510c-183">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="9510c-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="9510c-184">Valitse puusta "Invoice\EnclosedDocs\Document\FileName".</span><span class="sxs-lookup"><span data-stu-id="9510c-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="9510c-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-185">Click Bind.</span></span>
20. <span data-ttu-id="9510c-186">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="9510c-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="9510c-187">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="9510c-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="9510c-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="9510c-188">Click Bind.</span></span>
23. <span data-ttu-id="9510c-189">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9510c-189">Click Save.</span></span>
24. <span data-ttu-id="9510c-190">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9510c-190">Close the page.</span></span>


