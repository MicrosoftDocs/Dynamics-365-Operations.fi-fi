---
title: ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3 – muodon luominen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa. (Osa 3)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092613"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="41d42-104">ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3 – muodon luominen)</span><span class="sxs-lookup"><span data-stu-id="41d42-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41d42-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="41d42-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="41d42-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="41d42-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="41d42-107">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 2: laajenna tietomallia)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="41d42-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="41d42-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="41d42-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="41d42-109">Uuden muodon luonti laskujen käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="41d42-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="41d42-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="41d42-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="41d42-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="41d42-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="41d42-112">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="41d42-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="41d42-113">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="41d42-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="41d42-114">Luot muodon, jolla luodaan sähköisiä viestejä tiedostoista, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="41d42-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="41d42-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="41d42-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="41d42-116">Syötä Uusi-kenttään Muoto perustuu tietomalliin Myyntilaskumalli (mukautettu).</span><span class="sxs-lookup"><span data-stu-id="41d42-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="41d42-117">Kirjoita Nimi-kenttään "Sähköisen laskun malliviesti".</span><span class="sxs-lookup"><span data-stu-id="41d42-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="41d42-118">Sähköisen laskun esimerkkisanoma</span><span class="sxs-lookup"><span data-stu-id="41d42-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="41d42-119">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="41d42-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="41d42-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="41d42-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="41d42-121">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="41d42-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="41d42-122">Muodon suunnittelu, joka täyttää liitteet viestiin MIME-muodossa</span><span class="sxs-lookup"><span data-stu-id="41d42-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="41d42-123">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="41d42-123">Click Designer.</span></span>
2. <span data-ttu-id="41d42-124">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="41d42-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="41d42-125">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="41d42-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="41d42-126">Kirjoita Nimi-kenttään "Lasku".</span><span class="sxs-lookup"><span data-stu-id="41d42-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="41d42-127">Lasku</span><span class="sxs-lookup"><span data-stu-id="41d42-127">Invoice</span></span>  
5. <span data-ttu-id="41d42-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-128">Click OK.</span></span>
6. <span data-ttu-id="41d42-129">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="41d42-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="41d42-130">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="41d42-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="41d42-131">Syötä Nimi-kenttään "SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="41d42-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="41d42-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="41d42-132">SalesOrder</span></span>  
9. <span data-ttu-id="41d42-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-133">Click OK.</span></span>
10. <span data-ttu-id="41d42-134">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="41d42-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="41d42-135">Syötä Nimi-kenttään "InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="41d42-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="41d42-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="41d42-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="41d42-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-137">Click OK.</span></span>
13. <span data-ttu-id="41d42-138">Valitse Lisää määrite.</span><span class="sxs-lookup"><span data-stu-id="41d42-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="41d42-139">Kirjoita Nimi-kenttään "InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="41d42-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="41d42-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="41d42-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="41d42-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-141">Click OK.</span></span>
16. <span data-ttu-id="41d42-142">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="41d42-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="41d42-143">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="41d42-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="41d42-144">Kirjoita Nimi-kenttään "EnclosedDocs".</span><span class="sxs-lookup"><span data-stu-id="41d42-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="41d42-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="41d42-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="41d42-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-146">Click OK.</span></span>
20. <span data-ttu-id="41d42-147">Valitse puusta 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="41d42-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="41d42-148">Valitse Lisää elementti.</span><span class="sxs-lookup"><span data-stu-id="41d42-148">Click Add Element.</span></span>
22. <span data-ttu-id="41d42-149">Kirjoita Nimi-kenttään "Document".</span><span class="sxs-lookup"><span data-stu-id="41d42-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="41d42-150">Asiakirja</span><span class="sxs-lookup"><span data-stu-id="41d42-150">Document</span></span>  
23. <span data-ttu-id="41d42-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-151">Click OK.</span></span>
24. <span data-ttu-id="41d42-152">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="41d42-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="41d42-153">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="41d42-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="41d42-154">Valitse puussa solmu XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="41d42-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="41d42-155">Kirjoita Nimi-kenttään "FileName".</span><span class="sxs-lookup"><span data-stu-id="41d42-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="41d42-156">FileName</span><span class="sxs-lookup"><span data-stu-id="41d42-156">FileName</span></span>  
28. <span data-ttu-id="41d42-157">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-157">Click OK.</span></span>
29. <span data-ttu-id="41d42-158">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="41d42-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="41d42-159">Valitse puussa solmu XML\Element.</span><span class="sxs-lookup"><span data-stu-id="41d42-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="41d42-160">Kirjoita Nimi-kenttään "FileContent".</span><span class="sxs-lookup"><span data-stu-id="41d42-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="41d42-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="41d42-161">FileContent</span></span>  
32. <span data-ttu-id="41d42-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-162">Click OK.</span></span>
33. <span data-ttu-id="41d42-163">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent".</span><span class="sxs-lookup"><span data-stu-id="41d42-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="41d42-164">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="41d42-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="41d42-165">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="41d42-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="41d42-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="41d42-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="41d42-167">Yhdistä muodon elementit tietomalliin tietolähteenä</span><span class="sxs-lookup"><span data-stu-id="41d42-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="41d42-168">Valitse puusta "Invoice\SalesOrder".</span><span class="sxs-lookup"><span data-stu-id="41d42-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="41d42-169">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="41d42-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="41d42-170">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="41d42-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="41d42-171">Valitse puussa "model\Sales order number(SalesId)".</span><span class="sxs-lookup"><span data-stu-id="41d42-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="41d42-172">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-172">Click Bind.</span></span>
6. <span data-ttu-id="41d42-173">Valitse puusta "Invoice\InvoiceNumber".</span><span class="sxs-lookup"><span data-stu-id="41d42-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="41d42-174">Laajenna puussa "model\Base invoice(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="41d42-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="41d42-175">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice number(Id)".</span><span class="sxs-lookup"><span data-stu-id="41d42-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="41d42-176">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-176">Click Bind.</span></span>
10. <span data-ttu-id="41d42-177">Valitse puusta "Invoice\InvoiceAmount".</span><span class="sxs-lookup"><span data-stu-id="41d42-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="41d42-178">Valitse puusta "model\Base invoice(InvoiceBase)\Invoice amount(Amount)".</span><span class="sxs-lookup"><span data-stu-id="41d42-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="41d42-179">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-179">Click Bind.</span></span>
13. <span data-ttu-id="41d42-180">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="41d42-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="41d42-181">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="41d42-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="41d42-182">Valitse puusta "Invoice\EnclosedDocs\Document\FileContent\Base64".</span><span class="sxs-lookup"><span data-stu-id="41d42-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="41d42-183">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-183">Click Bind.</span></span>
17. <span data-ttu-id="41d42-184">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="41d42-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="41d42-185">Valitse puusta "Invoice\EnclosedDocs\Document\FileName".</span><span class="sxs-lookup"><span data-stu-id="41d42-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="41d42-186">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-186">Click Bind.</span></span>
20. <span data-ttu-id="41d42-187">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="41d42-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="41d42-188">Valitse puusta "Invoice\EnclosedDocs\Document".</span><span class="sxs-lookup"><span data-stu-id="41d42-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="41d42-189">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="41d42-189">Click Bind.</span></span>
23. <span data-ttu-id="41d42-190">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="41d42-190">Click Save.</span></span>
24. <span data-ttu-id="41d42-191">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="41d42-191">Close the page.</span></span>

