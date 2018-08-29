--- 
title: "Luo muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 934775bbdda13238e16fba91dcb90d6d3249e812
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="8d07d-103">Luo muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa</span><span class="sxs-lookup"><span data-stu-id="8d07d-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d07d-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="8d07d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="8d07d-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="8d07d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8d07d-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 2: laajenna tietomallia)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8d07d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="8d07d-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="8d07d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="8d07d-108">Uuden muodon luonti laskujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="8d07d-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="8d07d-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="8d07d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8d07d-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="8d07d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8d07d-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="8d07d-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="8d07d-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="8d07d-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="8d07d-113">Luot muodon, jolla luodaan sähköisiä viestejä tiedostoista, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="8d07d-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="8d07d-114">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="8d07d-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="8d07d-115">Syötä Uusi-kenttään Muoto perustuu tietomalliin Myyntilaskumalli (mukautettu).</span><span class="sxs-lookup"><span data-stu-id="8d07d-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="8d07d-116">Kirjoita Nimi-kenttään "Sähköisen laskun malliviesti".</span><span class="sxs-lookup"><span data-stu-id="8d07d-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="8d07d-117">Sähköisen laskun esimerkkisanoma</span><span class="sxs-lookup"><span data-stu-id="8d07d-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="8d07d-118">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="8d07d-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8d07d-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="8d07d-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="8d07d-120">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="8d07d-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="8d07d-121">Muodon suunnittelu, joka täyttää liitteet viestiin MIME-muodossa</span><span class="sxs-lookup"><span data-stu-id="8d07d-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="8d07d-122">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="8d07d-122">Click Designer.</span></span>
2. <span data-ttu-id="8d07d-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="8d07d-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="8d07d-124">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="8d07d-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="8d07d-125">Kirjoita Nimi-kenttään "Lasku".</span><span class="sxs-lookup"><span data-stu-id="8d07d-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="8d07d-126">Lasku</span><span class="sxs-lookup"><span data-stu-id="8d07d-126">Invoice</span></span>  
5. <span data-ttu-id="8d07d-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-127">Click OK.</span></span>
6. <span data-ttu-id="8d07d-128">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d07d-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="8d07d-129">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="8d07d-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="8d07d-130">Syötä Nimi-kenttään "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="8d07d-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="8d07d-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="8d07d-131">SalesOrder</span></span>  
9. <span data-ttu-id="8d07d-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-132">Click OK.</span></span>
10. <span data-ttu-id="8d07d-133">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="8d07d-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="8d07d-134">Syötä Nimi-kenttään "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="8d07d-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="8d07d-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="8d07d-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="8d07d-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-136">Click OK.</span></span>
13. <span data-ttu-id="8d07d-137">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="8d07d-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="8d07d-138">Kirjoita Nimi-kenttään "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="8d07d-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="8d07d-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="8d07d-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="8d07d-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-140">Click OK.</span></span>
16. <span data-ttu-id="8d07d-141">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d07d-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="8d07d-142">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="8d07d-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="8d07d-143">Kirjoita Nimi-kenttään "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="8d07d-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="8d07d-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="8d07d-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="8d07d-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-145">Click OK.</span></span>
20. <span data-ttu-id="8d07d-146">Valitse puusta 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="8d07d-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="8d07d-147">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="8d07d-147">Click Add Element.</span></span>
22. <span data-ttu-id="8d07d-148">Kirjoita Nimi-kenttään "Document".</span><span class="sxs-lookup"><span data-stu-id="8d07d-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="8d07d-149">Asiakirja</span><span class="sxs-lookup"><span data-stu-id="8d07d-149">Document</span></span>  
23. <span data-ttu-id="8d07d-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-150">Click OK.</span></span>
24. <span data-ttu-id="8d07d-151">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="8d07d-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="8d07d-152">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d07d-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="8d07d-153">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="8d07d-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="8d07d-154">Kirjoita Nimi-kenttään "FileName".</span><span class="sxs-lookup"><span data-stu-id="8d07d-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="8d07d-155">FileName</span><span class="sxs-lookup"><span data-stu-id="8d07d-155">FileName</span></span>  
28. <span data-ttu-id="8d07d-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-156">Click OK.</span></span>
29. <span data-ttu-id="8d07d-157">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d07d-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="8d07d-158">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="8d07d-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="8d07d-159">Kirjoita Nimi-kenttään "FileContent".</span><span class="sxs-lookup"><span data-stu-id="8d07d-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="8d07d-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="8d07d-160">FileContent</span></span>  
32. <span data-ttu-id="8d07d-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-161">Click OK.</span></span>
33. <span data-ttu-id="8d07d-162">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent".</span><span class="sxs-lookup"><span data-stu-id="8d07d-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="8d07d-163">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d07d-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="8d07d-164">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="8d07d-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="8d07d-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d07d-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="8d07d-166">Yhdistä muodon elementit tietomalliin tietolähteenä</span><span class="sxs-lookup"><span data-stu-id="8d07d-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="8d07d-167">Valitse puusta "Invoice\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="8d07d-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="8d07d-168">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8d07d-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="8d07d-169">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="8d07d-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="8d07d-170">Valitse puussa "model\Sales order number(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="8d07d-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="8d07d-171">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-171">Click Bind.</span></span>
6. <span data-ttu-id="8d07d-172">Valitse puusta "Invoice\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="8d07d-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="8d07d-173">Laajenna puussa "model\Base invoice(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="8d07d-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="8d07d-174">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice number(Id)".</span><span class="sxs-lookup"><span data-stu-id="8d07d-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="8d07d-175">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-175">Click Bind.</span></span>
10. <span data-ttu-id="8d07d-176">Valitse puusta "Invoice\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="8d07d-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="8d07d-177">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice amount(Amount)".</span><span class="sxs-lookup"><span data-stu-id="8d07d-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="8d07d-178">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-178">Click Bind.</span></span>
13. <span data-ttu-id="8d07d-179">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="8d07d-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="8d07d-180">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="8d07d-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="8d07d-181">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="8d07d-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="8d07d-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-182">Click Bind.</span></span>
17. <span data-ttu-id="8d07d-183">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="8d07d-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="8d07d-184">Valitse puusta "Invoice\EnclosedDocs\Document\FileName".</span><span class="sxs-lookup"><span data-stu-id="8d07d-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="8d07d-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-185">Click Bind.</span></span>
20. <span data-ttu-id="8d07d-186">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="8d07d-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="8d07d-187">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="8d07d-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="8d07d-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d07d-188">Click Bind.</span></span>
23. <span data-ttu-id="8d07d-189">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d07d-189">Click Save.</span></span>
24. <span data-ttu-id="8d07d-190">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d07d-190">Close the page.</span></span>


