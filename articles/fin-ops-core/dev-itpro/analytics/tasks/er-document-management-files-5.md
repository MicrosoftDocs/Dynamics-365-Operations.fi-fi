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
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182505"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="c8c7b-103">ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 5: muodon muokkaaminen ja suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="c8c7b-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8c7b-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c8c7b-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c8c7b-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 4: Suorita muoto)" -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="c8c7b-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="c8c7b-108">Muokkaa muotoa täyttämään liitteet tuottaviin viesteihin binäärimuodossa.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="c8c7b-109">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c8c7b-110">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="c8c7b-111">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="c8c7b-112">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="c8c7b-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-113">Click Designer.</span></span>
    * <span data-ttu-id="c8c7b-114">Laskuviesti täytetään Unicode-koodatulla XML-tiedoston tulosteella.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="c8c7b-115">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="c8c7b-116">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="c8c7b-117">Syötä Nimi-kenttään Xml-sanoma.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="c8c7b-118">Xml-sanoma</span><span class="sxs-lookup"><span data-stu-id="c8c7b-118">Xml message</span></span>  
9. <span data-ttu-id="c8c7b-119">Syötä Koodaus-kenttään UTF-8.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c8c7b-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c8c7b-120">UTF-8</span></span>  
10. <span data-ttu-id="c8c7b-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-121">Click OK.</span></span>
    * <span data-ttu-id="c8c7b-122">Konfiguroi tulosten luominen zip-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="c8c7b-123">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="c8c7b-124">Valitse puussa solmu Common\Folder.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="c8c7b-125">Syötä Nimi-kenttään Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="c8c7b-126">Zip-tulos</span><span class="sxs-lookup"><span data-stu-id="c8c7b-126">Zip output</span></span>  
14. <span data-ttu-id="c8c7b-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-127">Click OK.</span></span>
15. <span data-ttu-id="c8c7b-128">Valitse puussa Zip-tulos.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="c8c7b-129">Lisää liitteet luonnin zip-tiedostoon tiedostoina, joilla on niiden alkuperäiset nimet ja tiedostopäätteet.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="c8c7b-130">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c8c7b-131">Valitse puussa solmu Common\File.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="c8c7b-132">Kirjoita Nimi-kenttään Liitetiedosto.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="c8c7b-133">Liitetiedosto</span><span class="sxs-lookup"><span data-stu-id="c8c7b-133">Attached file</span></span>  
19. <span data-ttu-id="c8c7b-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-134">Click OK.</span></span>
20. <span data-ttu-id="c8c7b-135">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="c8c7b-136">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="c8c7b-137">Valitse puussa "Text\Base64".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="c8c7b-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="c8c7b-139">Uusien muotoelementtien yhdistäminen tietomalliin</span><span class="sxs-lookup"><span data-stu-id="c8c7b-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="c8c7b-140">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c8c7b-141">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="c8c7b-142">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="c8c7b-143">Valitse puusta 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="c8c7b-144">Valitse puussa "model\Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="c8c7b-145">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-145">Click Bind.</span></span>
7. <span data-ttu-id="c8c7b-146">Valitse puusta 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="c8c7b-147">Valitse Muokkaa tiedostonimeä.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-147">Click Edit filename.</span></span>
9. <span data-ttu-id="c8c7b-148">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="c8c7b-149">Laajenna puussa "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="c8c7b-150">Valitse puussa "model\Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="c8c7b-151">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-151">Click Add data source.</span></span>
13. <span data-ttu-id="c8c7b-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-152">Click Save.</span></span>
14. <span data-ttu-id="c8c7b-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-153">Close the page.</span></span>
15. <span data-ttu-id="c8c7b-154">Valitse puussa solmu "model\Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="c8c7b-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="c8c7b-155">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-155">Click Bind.</span></span>
17. <span data-ttu-id="c8c7b-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-156">Click Save.</span></span>
18. <span data-ttu-id="c8c7b-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="c8c7b-158">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="c8c7b-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="c8c7b-159">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-159">Click Run.</span></span>
2. <span data-ttu-id="c8c7b-160">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="c8c7b-161">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-161">Click Filter.</span></span>
4. <span data-ttu-id="c8c7b-162">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="c8c7b-163">Kirjoita Myyntitilaus-ehtokenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="c8c7b-164">000148</span><span class="sxs-lookup"><span data-stu-id="c8c7b-164">000148</span></span>  
6. <span data-ttu-id="c8c7b-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-165">Click OK.</span></span>
7. <span data-ttu-id="c8c7b-166">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-166">Click OK.</span></span>
    * <span data-ttu-id="c8c7b-167">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-167">Review the generated output.</span></span> <span data-ttu-id="c8c7b-168">Huomaa, että XML-muotoisen laskuviestin lisäksi jokaiselle liitteelle on luotu yksi tiedosto.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="c8c7b-169">Liitetiedostot täytetään pakatulla, binäärimuotoisella tulosteella.</span><span class="sxs-lookup"><span data-stu-id="c8c7b-169">The attachment files are populated with the zipped output in binary format.</span></span>  

