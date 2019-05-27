---
title: ER Tiedostonhallinnan tiedostojen käyttö muodon tuotoksissa (Osa 2 – Tietomallin laajentaminen)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544799"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="cde5b-103">ER Tiedostojenhallinnan tiedostojen käyttö muodon tuloksissa (osa 2: tietomallin laajennus)</span><span class="sxs-lookup"><span data-stu-id="cde5b-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cde5b-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="cde5b-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="cde5b-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="cde5b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="cde5b-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="cde5b-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="cde5b-107">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="cde5b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="cde5b-108">Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää</span><span class="sxs-lookup"><span data-stu-id="cde5b-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="cde5b-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="cde5b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cde5b-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="cde5b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cde5b-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="cde5b-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="cde5b-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="cde5b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="cde5b-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="cde5b-113">Click Designer.</span></span>
6. <span data-ttu-id="cde5b-114">Valitse puussa "Customer invoice(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="cde5b-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="cde5b-115">Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="cde5b-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="cde5b-116">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="cde5b-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="cde5b-117">Kirjoita Nimi-kenttään "Laskun liitteet".</span><span class="sxs-lookup"><span data-stu-id="cde5b-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="cde5b-118">Laskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="cde5b-118">Invoice attachments</span></span>  
9. <span data-ttu-id="cde5b-119">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="cde5b-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="cde5b-120">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="cde5b-120">Click Add.</span></span>
11. <span data-ttu-id="cde5b-121">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="cde5b-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="cde5b-122">Kirjoita Nimi-kenttään "Tiedostosisältö".</span><span class="sxs-lookup"><span data-stu-id="cde5b-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="cde5b-123">Tiedoston sisältö</span><span class="sxs-lookup"><span data-stu-id="cde5b-123">File content</span></span>  
13. <span data-ttu-id="cde5b-124">Valitse Nimiketyyppi-kenttään "Säilö".</span><span class="sxs-lookup"><span data-stu-id="cde5b-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="cde5b-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="cde5b-125">Click Add.</span></span>
15. <span data-ttu-id="cde5b-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="cde5b-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="cde5b-127">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="cde5b-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="cde5b-128">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="cde5b-128">File name</span></span>  
17. <span data-ttu-id="cde5b-129">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="cde5b-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="cde5b-130">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="cde5b-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="cde5b-131">Yhdistä uuden tietomallin elementit Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="cde5b-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="cde5b-132">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="cde5b-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="cde5b-133">Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="cde5b-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="cde5b-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="cde5b-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="cde5b-135">Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="cde5b-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="cde5b-136">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="cde5b-136">Click Designer.</span></span>
4. <span data-ttu-id="cde5b-137">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="cde5b-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="cde5b-138">Laajenna puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="cde5b-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="cde5b-139">Valitse puussa solmu "Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="cde5b-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="cde5b-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="cde5b-140">Click Edit.</span></span>
8. <span data-ttu-id="cde5b-141">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="cde5b-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="cde5b-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="cde5b-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="cde5b-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cde5b-143">Click Save.</span></span>
10. <span data-ttu-id="cde5b-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-144">Close the page.</span></span>
11. <span data-ttu-id="cde5b-145">Valitse puussa solmu "Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="cde5b-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="cde5b-146">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="cde5b-146">Click Edit.</span></span>
13. <span data-ttu-id="cde5b-147">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="cde5b-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="cde5b-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="cde5b-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="cde5b-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cde5b-149">Click Save.</span></span>
15. <span data-ttu-id="cde5b-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-150">Close the page.</span></span>
16. <span data-ttu-id="cde5b-151">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="cde5b-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="cde5b-152">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="cde5b-152">Click Edit.</span></span>
18. <span data-ttu-id="cde5b-153">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="cde5b-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="cde5b-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="cde5b-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="cde5b-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cde5b-155">Click Save.</span></span>
20. <span data-ttu-id="cde5b-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-156">Close the page.</span></span>
21. <span data-ttu-id="cde5b-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cde5b-157">Click Save.</span></span>
22. <span data-ttu-id="cde5b-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-158">Close the page.</span></span>
23. <span data-ttu-id="cde5b-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-159">Close the page.</span></span>
24. <span data-ttu-id="cde5b-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cde5b-160">Close the page.</span></span>
25. <span data-ttu-id="cde5b-161">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="cde5b-161">Click Change status.</span></span>
26. <span data-ttu-id="cde5b-162">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="cde5b-162">Click Complete.</span></span>
27. <span data-ttu-id="cde5b-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cde5b-163">Click OK.</span></span>

