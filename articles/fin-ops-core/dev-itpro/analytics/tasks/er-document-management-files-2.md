---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja (liitteitä) ER-tuotoksissa. (Osa 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754911"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="e1b08-104">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)</span><span class="sxs-lookup"><span data-stu-id="e1b08-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1b08-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="e1b08-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e1b08-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e1b08-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e1b08-107">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="e1b08-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="e1b08-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="e1b08-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="e1b08-109">Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää</span><span class="sxs-lookup"><span data-stu-id="e1b08-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="e1b08-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="e1b08-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e1b08-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="e1b08-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e1b08-112">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="e1b08-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="e1b08-113">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="e1b08-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="e1b08-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e1b08-114">Click Designer.</span></span>
6. <span data-ttu-id="e1b08-115">Valitse puussa "Customer invoice(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="e1b08-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="e1b08-116">Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="e1b08-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="e1b08-117">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1b08-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e1b08-118">Kirjoita Nimi-kenttään "Laskun liitteet".</span><span class="sxs-lookup"><span data-stu-id="e1b08-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="e1b08-119">Laskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="e1b08-119">Invoice attachments</span></span>  
9. <span data-ttu-id="e1b08-120">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="e1b08-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="e1b08-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e1b08-121">Click Add.</span></span>
11. <span data-ttu-id="e1b08-122">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1b08-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e1b08-123">Kirjoita Nimi-kenttään "Tiedostosisältö".</span><span class="sxs-lookup"><span data-stu-id="e1b08-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="e1b08-124">Tiedoston sisältö</span><span class="sxs-lookup"><span data-stu-id="e1b08-124">File content</span></span>  
13. <span data-ttu-id="e1b08-125">Valitse Nimiketyyppi-kenttään "Säilö".</span><span class="sxs-lookup"><span data-stu-id="e1b08-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="e1b08-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e1b08-126">Click Add.</span></span>
15. <span data-ttu-id="e1b08-127">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1b08-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="e1b08-128">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="e1b08-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e1b08-129">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="e1b08-129">File name</span></span>  
17. <span data-ttu-id="e1b08-130">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e1b08-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="e1b08-131">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e1b08-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="e1b08-132">Yhdistä uudet tietomallielementit tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="e1b08-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="e1b08-133">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="e1b08-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="e1b08-134">Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="e1b08-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="e1b08-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="e1b08-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="e1b08-136">Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="e1b08-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="e1b08-137">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e1b08-137">Click Designer.</span></span>
4. <span data-ttu-id="e1b08-138">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e1b08-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="e1b08-139">Laajenna puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e1b08-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="e1b08-140">Valitse puussa solmu "Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="e1b08-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="e1b08-141">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e1b08-141">Click Edit.</span></span>
8. <span data-ttu-id="e1b08-142">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="e1b08-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="e1b08-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="e1b08-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="e1b08-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1b08-144">Click Save.</span></span>
10. <span data-ttu-id="e1b08-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-145">Close the page.</span></span>
11. <span data-ttu-id="e1b08-146">Valitse puussa solmu "Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="e1b08-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="e1b08-147">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e1b08-147">Click Edit.</span></span>
13. <span data-ttu-id="e1b08-148">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="e1b08-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="e1b08-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="e1b08-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="e1b08-150">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1b08-150">Click Save.</span></span>
15. <span data-ttu-id="e1b08-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-151">Close the page.</span></span>
16. <span data-ttu-id="e1b08-152">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e1b08-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="e1b08-153">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e1b08-153">Click Edit.</span></span>
18. <span data-ttu-id="e1b08-154">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="e1b08-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="e1b08-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="e1b08-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="e1b08-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1b08-156">Click Save.</span></span>
20. <span data-ttu-id="e1b08-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-157">Close the page.</span></span>
21. <span data-ttu-id="e1b08-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1b08-158">Click Save.</span></span>
22. <span data-ttu-id="e1b08-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-159">Close the page.</span></span>
23. <span data-ttu-id="e1b08-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-160">Close the page.</span></span>
24. <span data-ttu-id="e1b08-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e1b08-161">Close the page.</span></span>
25. <span data-ttu-id="e1b08-162">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="e1b08-162">Click Change status.</span></span>
26. <span data-ttu-id="e1b08-163">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="e1b08-163">Click Complete.</span></span>
27. <span data-ttu-id="e1b08-164">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e1b08-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]