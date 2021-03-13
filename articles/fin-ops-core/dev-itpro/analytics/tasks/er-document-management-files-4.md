---
title: ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 4 – muodon suorittaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa. (Osa 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d437b31b8a55f345ebc3567bc8c6a2c5ecfd2eec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092513"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="3f7a8-104">ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 4 – muodon suorittaminen)</span><span class="sxs-lookup"><span data-stu-id="3f7a8-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f7a8-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="3f7a8-106">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="3f7a8-107">Jotta voit suorittaa nämä vaiheet, suorita ensin "ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3: muodon luominen)" -ohjeen vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="3f7a8-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="3f7a8-109">Lisää tarpeelliset liitteet yhden laskun myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="3f7a8-110">Siirry kohtaan Myyntireskontra > Laskut > Avoimet myyntilaskut.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="3f7a8-111">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3f7a8-112">Voit esimerkiksi suodattaa Lasku-kenttää arvolla CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="3f7a8-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="3f7a8-113">CIV-000148</span></span>  
3. <span data-ttu-id="3f7a8-114">Napsauta valitun laskun linkkiä avataksesi sen.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="3f7a8-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="3f7a8-115">CIV-000148</span></span>  
4. <span data-ttu-id="3f7a8-116">Siirry eteenpäin napsauttamalla Myyntitilaus-kentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="3f7a8-117">000148</span><span class="sxs-lookup"><span data-stu-id="3f7a8-117">000148</span></span>  
5. <span data-ttu-id="3f7a8-118">Valitse Rivit vai otsikko -kentästä vaihtoehto Otsikko.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="3f7a8-119">Valitse Otsikko osoittamaan, että tämä on liitteiden lisäämisen kohde.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="3f7a8-120">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-120">Click Attach.</span></span>
    * <span data-ttu-id="3f7a8-121">Lisää joitakin liitetiedostoja tälle myyntitilaukselle.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="3f7a8-122">Käytä Tiedostonhallinnassa tuettuja tiedostotyyppejä (tiedostopäätteet DOCX, PDF, XML, JPG jne.).</span><span class="sxs-lookup"><span data-stu-id="3f7a8-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="3f7a8-123">Etsi ja valitse liitettävät tiedostot, jotka käsitellään liittyvän laskun kanssa sähköisessä ER-viestissä.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="3f7a8-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-124">Click New.</span></span>
8. <span data-ttu-id="3f7a8-125">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-125">Click File.</span></span>
9. <span data-ttu-id="3f7a8-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-126">Click New.</span></span>
10. <span data-ttu-id="3f7a8-127">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-127">Click File.</span></span>
11. <span data-ttu-id="3f7a8-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-128">Close the page.</span></span>
12. <span data-ttu-id="3f7a8-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-129">Close the page.</span></span>
13. <span data-ttu-id="3f7a8-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-130">Close the page.</span></span>
14. <span data-ttu-id="3f7a8-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="3f7a8-132">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="3f7a8-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="3f7a8-133">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3f7a8-134">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="3f7a8-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="3f7a8-135">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="3f7a8-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="3f7a8-136">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="3f7a8-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="3f7a8-137">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-137">Click Run.</span></span>
6. <span data-ttu-id="3f7a8-138">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="3f7a8-139">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-139">Click Filter.</span></span>
8. <span data-ttu-id="3f7a8-140">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="3f7a8-141">Kirjoita Ehdot-kenttään 000148.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="3f7a8-142">Kirjoita ehdoksi "Sales order" -kenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="3f7a8-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-143">Click OK.</span></span>
11. <span data-ttu-id="3f7a8-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-144">Click OK.</span></span>
    * <span data-ttu-id="3f7a8-145">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-145">Review the generated output.</span></span> <span data-ttu-id="3f7a8-146">Huomaa, että kullekin liitetiedostolle on luotu yksi XML-solmu.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="3f7a8-147">Liitteen sisältö lisätään XML-tuotteeseen MIME (base64) -tekstimuodossa.</span><span class="sxs-lookup"><span data-stu-id="3f7a8-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

