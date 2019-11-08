---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 5 – Muodon muokkaaminen ja suorittaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550691"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="c6f0f-103">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 5 – Muodon muokkaaminen ja suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="c6f0f-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6f0f-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c6f0f-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c6f0f-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 4: Suorita muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="c6f0f-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="c6f0f-108">Muokkaa muotoa täyttämään liitteet tuottaviin viesteihin binäärimuodossa.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="c6f0f-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c6f0f-110">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="c6f0f-111">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="c6f0f-112">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="c6f0f-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-113">Click Designer.</span></span>
    * <span data-ttu-id="c6f0f-114">Laskuviesti täytetään Unicode-koodatulla XML-tiedoston tulosteella.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="c6f0f-115">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="c6f0f-116">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="c6f0f-117">Syötä Nimi-kenttään Xml-sanoma.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="c6f0f-118">Xml-sanoma</span><span class="sxs-lookup"><span data-stu-id="c6f0f-118">Xml message</span></span>  
9. <span data-ttu-id="c6f0f-119">Syötä Koodaus-kenttään UTF-8.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c6f0f-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c6f0f-120">UTF-8</span></span>  
10. <span data-ttu-id="c6f0f-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-121">Click OK.</span></span>
    * <span data-ttu-id="c6f0f-122">Konfiguroi tulosten luominen zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="c6f0f-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="c6f0f-124">Valitse puussa solmu Common\Folder.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="c6f0f-125">Syötä Nimi-kenttään Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="c6f0f-126">Zip-tulos</span><span class="sxs-lookup"><span data-stu-id="c6f0f-126">Zip output</span></span>  
14. <span data-ttu-id="c6f0f-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-127">Click OK.</span></span>
15. <span data-ttu-id="c6f0f-128">Valitse puussa Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="c6f0f-129">Lisää liitteet luonnin zip-tiedostoon tiedostoina, joilla on niiden alkuperäiset nimet ja tiedostopäätteet.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="c6f0f-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c6f0f-131">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="c6f0f-132">Kirjoita Nimi-kenttään Liitetiedosto.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="c6f0f-133">Liitetiedosto</span><span class="sxs-lookup"><span data-stu-id="c6f0f-133">Attached file</span></span>  
19. <span data-ttu-id="c6f0f-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-134">Click OK.</span></span>
20. <span data-ttu-id="c6f0f-135">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="c6f0f-136">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="c6f0f-137">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="c6f0f-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="c6f0f-139">Uusien muotoelementtien yhdistäminen tietomalliin</span><span class="sxs-lookup"><span data-stu-id="c6f0f-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="c6f0f-140">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c6f0f-141">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="c6f0f-142">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="c6f0f-143">Valitse puusta 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="c6f0f-144">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="c6f0f-145">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-145">Click Bind.</span></span>
7. <span data-ttu-id="c6f0f-146">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="c6f0f-147">Valitse Muokkaa tiedostonimeä.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-147">Click Edit filename.</span></span>
9. <span data-ttu-id="c6f0f-148">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="c6f0f-149">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="c6f0f-150">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="c6f0f-151">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-151">Click Add data source.</span></span>
13. <span data-ttu-id="c6f0f-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-152">Click Save.</span></span>
14. <span data-ttu-id="c6f0f-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-153">Close the page.</span></span>
15. <span data-ttu-id="c6f0f-154">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c6f0f-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="c6f0f-155">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-155">Click Bind.</span></span>
17. <span data-ttu-id="c6f0f-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-156">Click Save.</span></span>
18. <span data-ttu-id="c6f0f-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="c6f0f-158">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="c6f0f-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="c6f0f-159">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-159">Click Run.</span></span>
2. <span data-ttu-id="c6f0f-160">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="c6f0f-161">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-161">Click Filter.</span></span>
4. <span data-ttu-id="c6f0f-162">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="c6f0f-163">Kirjoita Myyntitilaus-ehtokenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="c6f0f-164">000148</span><span class="sxs-lookup"><span data-stu-id="c6f0f-164">000148</span></span>  
6. <span data-ttu-id="c6f0f-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-165">Click OK.</span></span>
7. <span data-ttu-id="c6f0f-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-166">Click OK.</span></span>
    * <span data-ttu-id="c6f0f-167">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-167">Review the generated output.</span></span> <span data-ttu-id="c6f0f-168">Huomaa, että XML-muotoisen laskuviestin lisäksi jokaiselle liitteelle on luotu yksi tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="c6f0f-169">Liitetiedostot täytetään pakatulla, binäärimuotoisella tulosteella.</span><span class="sxs-lookup"><span data-stu-id="c6f0f-169">The attachment files are populated with the zipped output in binary format.</span></span>  

