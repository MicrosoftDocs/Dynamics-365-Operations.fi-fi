---
title: Luo muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05c0c4a38f34774e7018504c5e3fab834a2ec1b1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850276"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3-create-format"></a><span data-ttu-id="1c664-103">ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3: muodon luominen)</span><span class="sxs-lookup"><span data-stu-id="1c664-103">ER Use Document Management files in format outputs (Part 3: Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c664-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="1c664-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1c664-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1c664-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1c664-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 2: laajenna tietomallia)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="1c664-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="1c664-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="1c664-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="1c664-108">Uuden muodon luonti laskujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="1c664-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="1c664-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="1c664-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1c664-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="1c664-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1c664-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="1c664-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="1c664-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="1c664-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="1c664-113">Luot muodon, jolla luodaan sähköisiä viestejä tiedostoista, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="1c664-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="1c664-114">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="1c664-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="1c664-115">Syötä Uusi-kenttään Muoto perustuu tietomalliin Myyntilaskumalli (mukautettu).</span><span class="sxs-lookup"><span data-stu-id="1c664-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="1c664-116">Kirjoita Nimi-kenttään "Sähköisen laskun malliviesti".</span><span class="sxs-lookup"><span data-stu-id="1c664-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="1c664-117">Sähköisen laskun esimerkkisanoma</span><span class="sxs-lookup"><span data-stu-id="1c664-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="1c664-118">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="1c664-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="1c664-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="1c664-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="1c664-120">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="1c664-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="1c664-121">Muodon suunnittelu, joka täyttää liitteet viestiin MIME-muodossa</span><span class="sxs-lookup"><span data-stu-id="1c664-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="1c664-122">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="1c664-122">Click Designer.</span></span>
2. <span data-ttu-id="1c664-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="1c664-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="1c664-124">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1c664-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="1c664-125">Kirjoita Nimi-kenttään "Lasku".</span><span class="sxs-lookup"><span data-stu-id="1c664-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="1c664-126">Lasku</span><span class="sxs-lookup"><span data-stu-id="1c664-126">Invoice</span></span>  
5. <span data-ttu-id="1c664-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-127">Click OK.</span></span>
6. <span data-ttu-id="1c664-128">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="1c664-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="1c664-129">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1c664-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="1c664-130">Syötä Nimi-kenttään "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="1c664-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="1c664-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="1c664-131">SalesOrder</span></span>  
9. <span data-ttu-id="1c664-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-132">Click OK.</span></span>
10. <span data-ttu-id="1c664-133">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="1c664-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="1c664-134">Syötä Nimi-kenttään "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="1c664-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="1c664-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="1c664-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="1c664-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-136">Click OK.</span></span>
13. <span data-ttu-id="1c664-137">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="1c664-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="1c664-138">Kirjoita Nimi-kenttään "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="1c664-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="1c664-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="1c664-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="1c664-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-140">Click OK.</span></span>
16. <span data-ttu-id="1c664-141">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="1c664-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="1c664-142">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1c664-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="1c664-143">Kirjoita Nimi-kenttään "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="1c664-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="1c664-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="1c664-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="1c664-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-145">Click OK.</span></span>
20. <span data-ttu-id="1c664-146">Valitse puusta 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="1c664-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="1c664-147">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="1c664-147">Click Add Element.</span></span>
22. <span data-ttu-id="1c664-148">Kirjoita Nimi-kenttään "Document".</span><span class="sxs-lookup"><span data-stu-id="1c664-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="1c664-149">Asiakirja</span><span class="sxs-lookup"><span data-stu-id="1c664-149">Document</span></span>  
23. <span data-ttu-id="1c664-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-150">Click OK.</span></span>
24. <span data-ttu-id="1c664-151">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="1c664-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="1c664-152">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="1c664-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="1c664-153">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1c664-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="1c664-154">Kirjoita Nimi-kenttään "FileName".</span><span class="sxs-lookup"><span data-stu-id="1c664-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="1c664-155">FileName</span><span class="sxs-lookup"><span data-stu-id="1c664-155">FileName</span></span>  
28. <span data-ttu-id="1c664-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-156">Click OK.</span></span>
29. <span data-ttu-id="1c664-157">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="1c664-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="1c664-158">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1c664-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="1c664-159">Kirjoita Nimi-kenttään "FileContent".</span><span class="sxs-lookup"><span data-stu-id="1c664-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="1c664-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="1c664-160">FileContent</span></span>  
32. <span data-ttu-id="1c664-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-161">Click OK.</span></span>
33. <span data-ttu-id="1c664-162">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent".</span><span class="sxs-lookup"><span data-stu-id="1c664-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="1c664-163">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="1c664-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="1c664-164">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="1c664-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="1c664-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1c664-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="1c664-166">Yhdistä muodon elementit tietomalliin tietolähteenä</span><span class="sxs-lookup"><span data-stu-id="1c664-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="1c664-167">Valitse puusta "Invoice\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="1c664-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="1c664-168">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1c664-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="1c664-169">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="1c664-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="1c664-170">Valitse puussa "model\Sales order number(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="1c664-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="1c664-171">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-171">Click Bind.</span></span>
6. <span data-ttu-id="1c664-172">Valitse puusta "Invoice\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="1c664-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="1c664-173">Laajenna puussa "model\Base invoice(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="1c664-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="1c664-174">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice number(Id)".</span><span class="sxs-lookup"><span data-stu-id="1c664-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="1c664-175">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-175">Click Bind.</span></span>
10. <span data-ttu-id="1c664-176">Valitse puusta "Invoice\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="1c664-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="1c664-177">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice amount(Amount)".</span><span class="sxs-lookup"><span data-stu-id="1c664-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="1c664-178">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-178">Click Bind.</span></span>
13. <span data-ttu-id="1c664-179">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="1c664-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="1c664-180">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="1c664-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="1c664-181">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="1c664-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="1c664-182">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-182">Click Bind.</span></span>
17. <span data-ttu-id="1c664-183">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="1c664-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="1c664-184">Valitse puusta "Invoice\EnclosedDocs\Document\FileName".</span><span class="sxs-lookup"><span data-stu-id="1c664-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="1c664-185">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-185">Click Bind.</span></span>
20. <span data-ttu-id="1c664-186">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="1c664-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="1c664-187">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="1c664-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="1c664-188">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="1c664-188">Click Bind.</span></span>
23. <span data-ttu-id="1c664-189">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1c664-189">Click Save.</span></span>
24. <span data-ttu-id="1c664-190">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1c664-190">Close the page.</span></span>

