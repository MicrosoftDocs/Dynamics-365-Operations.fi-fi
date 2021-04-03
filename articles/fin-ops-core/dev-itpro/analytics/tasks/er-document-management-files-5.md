---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 5 – Muodon muokkaaminen ja suorittaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja (liitteitä) ER-tuotoksissa. (Osa 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6062945dfea0eec02e5055e9ebe697189267e051
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564807"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="0e5cf-104">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 5 – Muodon muokkaaminen ja suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="0e5cf-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e5cf-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0e5cf-106">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0e5cf-107">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 4: Suorita muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="0e5cf-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="0e5cf-109">Muokkaa muotoa täyttämään liitteet tuottaviin viesteihin binäärimuodossa.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="0e5cf-110">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0e5cf-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="0e5cf-112">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0e5cf-113">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="0e5cf-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-114">Click Designer.</span></span>
    * <span data-ttu-id="0e5cf-115">Laskuviesti täytetään Unicode-koodatulla XML-tiedoston tulosteella.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="0e5cf-116">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="0e5cf-117">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="0e5cf-118">Syötä Nimi-kenttään Xml-sanoma.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="0e5cf-119">Xml-sanoma</span><span class="sxs-lookup"><span data-stu-id="0e5cf-119">Xml message</span></span>  
9. <span data-ttu-id="0e5cf-120">Syötä Koodaus-kenttään UTF-8.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0e5cf-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0e5cf-121">UTF-8</span></span>  
10. <span data-ttu-id="0e5cf-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-122">Click OK.</span></span>
    * <span data-ttu-id="0e5cf-123">Konfiguroi tulosten luominen zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="0e5cf-124">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="0e5cf-125">Valitse puussa solmu Common\Folder.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="0e5cf-126">Syötä Nimi-kenttään Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="0e5cf-127">Zip-tulos</span><span class="sxs-lookup"><span data-stu-id="0e5cf-127">Zip output</span></span>  
14. <span data-ttu-id="0e5cf-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-128">Click OK.</span></span>
15. <span data-ttu-id="0e5cf-129">Valitse puussa Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="0e5cf-130">Lisää liitteet luonnin zip-tiedostoon tiedostoina, joilla on niiden alkuperäiset nimet ja tiedostopäätteet.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="0e5cf-131">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0e5cf-132">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="0e5cf-133">Kirjoita Nimi-kenttään Liitetiedosto.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="0e5cf-134">Liitetiedosto</span><span class="sxs-lookup"><span data-stu-id="0e5cf-134">Attached file</span></span>  
19. <span data-ttu-id="0e5cf-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-135">Click OK.</span></span>
20. <span data-ttu-id="0e5cf-136">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="0e5cf-137">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="0e5cf-138">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="0e5cf-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="0e5cf-140">Uusien muotoelementtien yhdistäminen tietomalliin</span><span class="sxs-lookup"><span data-stu-id="0e5cf-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="0e5cf-141">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0e5cf-142">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="0e5cf-143">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="0e5cf-144">Valitse puusta 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="0e5cf-145">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="0e5cf-146">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-146">Click Bind.</span></span>
7. <span data-ttu-id="0e5cf-147">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="0e5cf-148">Valitse Muokkaa tiedostonimeä.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-148">Click Edit filename.</span></span>
9. <span data-ttu-id="0e5cf-149">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="0e5cf-150">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="0e5cf-151">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="0e5cf-152">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-152">Click Add data source.</span></span>
13. <span data-ttu-id="0e5cf-153">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-153">Click Save.</span></span>
14. <span data-ttu-id="0e5cf-154">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-154">Close the page.</span></span>
15. <span data-ttu-id="0e5cf-155">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="0e5cf-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="0e5cf-156">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-156">Click Bind.</span></span>
17. <span data-ttu-id="0e5cf-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-157">Click Save.</span></span>
18. <span data-ttu-id="0e5cf-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="0e5cf-159">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="0e5cf-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="0e5cf-160">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-160">Click Run.</span></span>
2. <span data-ttu-id="0e5cf-161">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="0e5cf-162">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-162">Click Filter.</span></span>
4. <span data-ttu-id="0e5cf-163">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="0e5cf-164">Kirjoita Myyntitilaus-ehtokenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="0e5cf-165">000148</span><span class="sxs-lookup"><span data-stu-id="0e5cf-165">000148</span></span>  
6. <span data-ttu-id="0e5cf-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-166">Click OK.</span></span>
7. <span data-ttu-id="0e5cf-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-167">Click OK.</span></span>
    * <span data-ttu-id="0e5cf-168">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-168">Review the generated output.</span></span> <span data-ttu-id="0e5cf-169">Huomaa, että XML-muotoisen laskuviestin lisäksi jokaiselle liitteelle on luotu yksi tiedosto.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="0e5cf-170">Liitetiedostot täytetään pakatulla, binäärimuotoisella tulosteella.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]