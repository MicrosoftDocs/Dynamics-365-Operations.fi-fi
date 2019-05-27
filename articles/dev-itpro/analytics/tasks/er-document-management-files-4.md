---
title: Aja muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544798"
---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="afecb-103">Aja muotoja tiedostonhallinnan tiedostojen käyttämiseksi ER-tuotoksissa</span><span class="sxs-lookup"><span data-stu-id="afecb-103">Run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afecb-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="afecb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="afecb-105">Nämä vaiheet voidaan suorittaa DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="afecb-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="afecb-106">Jotta voit suorittaa nämä vaiheet, suorita ensin "ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 3: muodon luominen)" -ohjeen vaiheet.</span><span class="sxs-lookup"><span data-stu-id="afecb-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="afecb-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="afecb-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="afecb-108">Lisää tarpeelliset liitteet yhden laskun myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="afecb-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="afecb-109">Siirry kohtaan Myyntireskontra > Laskut > Avoimet myyntilaskut.</span><span class="sxs-lookup"><span data-stu-id="afecb-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="afecb-110">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="afecb-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="afecb-111">Voit esimerkiksi suodattaa Lasku-kenttää arvolla CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="afecb-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="afecb-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="afecb-112">CIV-000148</span></span>  
3. <span data-ttu-id="afecb-113">Napsauta valitun laskun linkkiä avataksesi sen.</span><span class="sxs-lookup"><span data-stu-id="afecb-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="afecb-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="afecb-114">CIV-000148</span></span>  
4. <span data-ttu-id="afecb-115">Siirry eteenpäin napsauttamalla Myyntitilaus-kentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="afecb-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="afecb-116">000148</span><span class="sxs-lookup"><span data-stu-id="afecb-116">000148</span></span>  
5. <span data-ttu-id="afecb-117">Valitse Rivit vai otsikko -kentästä vaihtoehto Otsikko.</span><span class="sxs-lookup"><span data-stu-id="afecb-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="afecb-118">Valitse Otsikko osoittamaan, että tämä on liitteiden lisäämisen kohde.</span><span class="sxs-lookup"><span data-stu-id="afecb-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="afecb-119">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="afecb-119">Click Attach.</span></span>
    * <span data-ttu-id="afecb-120">Lisää joitakin liitetiedostoja tälle myyntitilaukselle.</span><span class="sxs-lookup"><span data-stu-id="afecb-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="afecb-121">Käytä Tiedostonhallinnassa tuettuja tiedostotyyppejä (tiedostopäätteet DOCX, PDF, XML, JPG jne.).</span><span class="sxs-lookup"><span data-stu-id="afecb-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="afecb-122">Etsi ja valitse liitettävät tiedostot, jotka käsitellään liittyvän laskun kanssa sähköisessä ER-viestissä.</span><span class="sxs-lookup"><span data-stu-id="afecb-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="afecb-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="afecb-123">Click New.</span></span>
8. <span data-ttu-id="afecb-124">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="afecb-124">Click File.</span></span>
9. <span data-ttu-id="afecb-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="afecb-125">Click New.</span></span>
10. <span data-ttu-id="afecb-126">Napsauta Tiedosto.</span><span class="sxs-lookup"><span data-stu-id="afecb-126">Click File.</span></span>
11. <span data-ttu-id="afecb-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="afecb-127">Close the page.</span></span>
12. <span data-ttu-id="afecb-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="afecb-128">Close the page.</span></span>
13. <span data-ttu-id="afecb-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="afecb-129">Close the page.</span></span>
14. <span data-ttu-id="afecb-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="afecb-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="afecb-131">Aja valitun laskun suunniteltu raportti</span><span class="sxs-lookup"><span data-stu-id="afecb-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="afecb-132">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="afecb-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="afecb-133">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="afecb-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="afecb-134">Laajenna puussa "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="afecb-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="afecb-135">Valitse puussa "Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message".</span><span class="sxs-lookup"><span data-stu-id="afecb-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="afecb-136">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="afecb-136">Click Run.</span></span>
6. <span data-ttu-id="afecb-137">Laajenna Tietueet-kohta ja sisällytä () -osa.</span><span class="sxs-lookup"><span data-stu-id="afecb-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="afecb-138">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="afecb-138">Click Filter.</span></span>
8. <span data-ttu-id="afecb-139">Valitse asiakkaan laskun kirjauskansion rivi sekä Myyntitilaus-kenttä.</span><span class="sxs-lookup"><span data-stu-id="afecb-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="afecb-140">Kirjoita Ehdot-kenttään 000148.</span><span class="sxs-lookup"><span data-stu-id="afecb-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="afecb-141">Kirjoita ehdoksi "Sales order" -kenttään tilausnumero 000148.</span><span class="sxs-lookup"><span data-stu-id="afecb-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="afecb-142">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="afecb-142">Click OK.</span></span>
11. <span data-ttu-id="afecb-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="afecb-143">Click OK.</span></span>
    * <span data-ttu-id="afecb-144">Tarkista aikaansaatu tuotos.</span><span class="sxs-lookup"><span data-stu-id="afecb-144">Review the generated output.</span></span> <span data-ttu-id="afecb-145">Huomaa, että kullekin liitetiedostolle on luotu yksi XML-solmu.</span><span class="sxs-lookup"><span data-stu-id="afecb-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="afecb-146">Liitteen sisältö lisätään XML-tuotteeseen MIME (base64) -tekstimuodossa.</span><span class="sxs-lookup"><span data-stu-id="afecb-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

