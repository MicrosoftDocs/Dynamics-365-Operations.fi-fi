---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon määrittämisestä käyttämään tiedostonhallinnan tiedostoja (liitteitä) ER-tuotoksissa. (Osa 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092587"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="e88ed-104">ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)</span><span class="sxs-lookup"><span data-stu-id="e88ed-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e88ed-105">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="e88ed-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e88ed-106">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e88ed-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e88ed-107">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="e88ed-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="e88ed-108">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="e88ed-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="e88ed-109">Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää</span><span class="sxs-lookup"><span data-stu-id="e88ed-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="e88ed-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="e88ed-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e88ed-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="e88ed-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e88ed-112">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="e88ed-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="e88ed-113">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="e88ed-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="e88ed-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e88ed-114">Click Designer.</span></span>
6. <span data-ttu-id="e88ed-115">Valitse puussa "Customer invoice(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="e88ed-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="e88ed-116">Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="e88ed-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="e88ed-117">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e88ed-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e88ed-118">Kirjoita Nimi-kenttään "Laskun liitteet".</span><span class="sxs-lookup"><span data-stu-id="e88ed-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="e88ed-119">Laskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="e88ed-119">Invoice attachments</span></span>  
9. <span data-ttu-id="e88ed-120">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="e88ed-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="e88ed-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e88ed-121">Click Add.</span></span>
11. <span data-ttu-id="e88ed-122">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e88ed-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e88ed-123">Kirjoita Nimi-kenttään "Tiedostosisältö".</span><span class="sxs-lookup"><span data-stu-id="e88ed-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="e88ed-124">Tiedoston sisältö</span><span class="sxs-lookup"><span data-stu-id="e88ed-124">File content</span></span>  
13. <span data-ttu-id="e88ed-125">Valitse Nimiketyyppi-kenttään "Säilö".</span><span class="sxs-lookup"><span data-stu-id="e88ed-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="e88ed-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e88ed-126">Click Add.</span></span>
15. <span data-ttu-id="e88ed-127">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e88ed-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="e88ed-128">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="e88ed-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e88ed-129">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="e88ed-129">File name</span></span>  
17. <span data-ttu-id="e88ed-130">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e88ed-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="e88ed-131">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e88ed-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="e88ed-132">Yhdistä uudet tietomallielementit tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="e88ed-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="e88ed-133">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="e88ed-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="e88ed-134">Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="e88ed-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="e88ed-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="e88ed-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="e88ed-136">Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="e88ed-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="e88ed-137">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e88ed-137">Click Designer.</span></span>
4. <span data-ttu-id="e88ed-138">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e88ed-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="e88ed-139">Laajenna puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e88ed-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="e88ed-140">Valitse puussa solmu "Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="e88ed-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="e88ed-141">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e88ed-141">Click Edit.</span></span>
8. <span data-ttu-id="e88ed-142">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="e88ed-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="e88ed-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="e88ed-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="e88ed-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e88ed-144">Click Save.</span></span>
10. <span data-ttu-id="e88ed-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-145">Close the page.</span></span>
11. <span data-ttu-id="e88ed-146">Valitse puussa solmu "Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="e88ed-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="e88ed-147">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e88ed-147">Click Edit.</span></span>
13. <span data-ttu-id="e88ed-148">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="e88ed-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="e88ed-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="e88ed-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="e88ed-150">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e88ed-150">Click Save.</span></span>
15. <span data-ttu-id="e88ed-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-151">Close the page.</span></span>
16. <span data-ttu-id="e88ed-152">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="e88ed-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="e88ed-153">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e88ed-153">Click Edit.</span></span>
18. <span data-ttu-id="e88ed-154">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="e88ed-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="e88ed-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="e88ed-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="e88ed-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e88ed-156">Click Save.</span></span>
20. <span data-ttu-id="e88ed-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-157">Close the page.</span></span>
21. <span data-ttu-id="e88ed-158">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e88ed-158">Click Save.</span></span>
22. <span data-ttu-id="e88ed-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-159">Close the page.</span></span>
23. <span data-ttu-id="e88ed-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-160">Close the page.</span></span>
24. <span data-ttu-id="e88ed-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e88ed-161">Close the page.</span></span>
25. <span data-ttu-id="e88ed-162">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="e88ed-162">Click Change status.</span></span>
26. <span data-ttu-id="e88ed-163">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="e88ed-163">Click Complete.</span></span>
27. <span data-ttu-id="e88ed-164">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e88ed-164">Click OK.</span></span>

