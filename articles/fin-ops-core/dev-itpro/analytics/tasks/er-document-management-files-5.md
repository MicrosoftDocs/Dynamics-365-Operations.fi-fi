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
ms.openlocfilehash: 1a52a7dd3b31c0189577422a79d47b318aae4a05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141993"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="740cc-103">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 5 – Muodon muokkaaminen ja suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="740cc-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="740cc-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="740cc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="740cc-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="740cc-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="740cc-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 4: Suorita muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="740cc-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="740cc-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="740cc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="740cc-108">Muokkaa muotoa täyttämään liitteet tuottaviin viesteihin binäärimuodossa.</span><span class="sxs-lookup"><span data-stu-id="740cc-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="740cc-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="740cc-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="740cc-110">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="740cc-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="740cc-111">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="740cc-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="740cc-112">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="740cc-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="740cc-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="740cc-113">Click Designer.</span></span>
    * <span data-ttu-id="740cc-114">Laskuviesti täytetään Unicode-koodatulla XML-tiedoston tulosteella.</span><span class="sxs-lookup"><span data-stu-id="740cc-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="740cc-115">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="740cc-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="740cc-116">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="740cc-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="740cc-117">Syötä Nimi-kenttään Xml-sanoma.</span><span class="sxs-lookup"><span data-stu-id="740cc-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="740cc-118">Xml-sanoma</span><span class="sxs-lookup"><span data-stu-id="740cc-118">Xml message</span></span>  
9. <span data-ttu-id="740cc-119">Syötä Koodaus-kenttään UTF-8.</span><span class="sxs-lookup"><span data-stu-id="740cc-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="740cc-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="740cc-120">UTF-8</span></span>  
10. <span data-ttu-id="740cc-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-121">Click OK.</span></span>
    * <span data-ttu-id="740cc-122">Konfiguroi tulosten luominen zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="740cc-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="740cc-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="740cc-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="740cc-124">Valitse puussa solmu Common\Folder.</span><span class="sxs-lookup"><span data-stu-id="740cc-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="740cc-125">Syötä Nimi-kenttään Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="740cc-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="740cc-126">Zip-tulos</span><span class="sxs-lookup"><span data-stu-id="740cc-126">Zip output</span></span>  
14. <span data-ttu-id="740cc-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-127">Click OK.</span></span>
15. <span data-ttu-id="740cc-128">Valitse puussa Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="740cc-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="740cc-129">Lisää liitteet luonnin zip-tiedostoon tiedostoina, joilla on niiden alkuperäiset nimet ja tiedostopäätteet.</span><span class="sxs-lookup"><span data-stu-id="740cc-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="740cc-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="740cc-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="740cc-131">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="740cc-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="740cc-132">Kirjoita Nimi-kenttään Liitetiedosto.</span><span class="sxs-lookup"><span data-stu-id="740cc-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="740cc-133">Liitetiedosto</span><span class="sxs-lookup"><span data-stu-id="740cc-133">Attached file</span></span>  
19. <span data-ttu-id="740cc-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-134">Click OK.</span></span>
20. <span data-ttu-id="740cc-135">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="740cc-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="740cc-136">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="740cc-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="740cc-137">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="740cc-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="740cc-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="740cc-139">Uusien muotoelementtien yhdistäminen tietomalliin</span><span class="sxs-lookup"><span data-stu-id="740cc-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="740cc-140">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="740cc-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="740cc-141">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="740cc-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="740cc-142">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="740cc-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="740cc-143">Valitse puusta 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="740cc-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="740cc-144">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="740cc-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="740cc-145">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="740cc-145">Click Bind.</span></span>
7. <span data-ttu-id="740cc-146">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="740cc-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="740cc-147">Valitse Muokkaa tiedostonimeä.</span><span class="sxs-lookup"><span data-stu-id="740cc-147">Click Edit filename.</span></span>
9. <span data-ttu-id="740cc-148">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="740cc-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="740cc-149">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="740cc-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="740cc-150">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="740cc-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="740cc-151">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="740cc-151">Click Add data source.</span></span>
13. <span data-ttu-id="740cc-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="740cc-152">Click Save.</span></span>
14. <span data-ttu-id="740cc-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="740cc-153">Close the page.</span></span>
15. <span data-ttu-id="740cc-154">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="740cc-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="740cc-155">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="740cc-155">Click Bind.</span></span>
17. <span data-ttu-id="740cc-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="740cc-156">Click Save.</span></span>
18. <span data-ttu-id="740cc-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="740cc-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="740cc-158">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="740cc-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="740cc-159">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="740cc-159">Click Run.</span></span>
2. <span data-ttu-id="740cc-160">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="740cc-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="740cc-161">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="740cc-161">Click Filter.</span></span>
4. <span data-ttu-id="740cc-162">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="740cc-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="740cc-163">Kirjoita Myyntitilaus-ehtokenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="740cc-163">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="740cc-164">000148</span><span class="sxs-lookup"><span data-stu-id="740cc-164">000148</span></span>  
6. <span data-ttu-id="740cc-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-165">Click OK.</span></span>
7. <span data-ttu-id="740cc-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="740cc-166">Click OK.</span></span>
    * <span data-ttu-id="740cc-167">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="740cc-167">Review the generated output.</span></span> <span data-ttu-id="740cc-168">Huomaa, että XML-muotoisen laskuviestin lisäksi jokaiselle liitteelle on luotu yksi tiedosto.</span><span class="sxs-lookup"><span data-stu-id="740cc-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="740cc-169">Liitetiedostot täytetään pakatulla, binäärimuotoisella tulosteella.</span><span class="sxs-lookup"><span data-stu-id="740cc-169">The attachment files are populated with the zipped output in binary format.</span></span>  

