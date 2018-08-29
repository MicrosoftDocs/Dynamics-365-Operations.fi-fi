--- 
title: "Laajenna tietomalli käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="3afc3-103">Laajenna tietomalli käyttämään tiedostonhallinnan tiedostoja ER-tuotoksissa</span><span class="sxs-lookup"><span data-stu-id="3afc3-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3afc3-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="3afc3-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="3afc3-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="3afc3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3afc3-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3afc3-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="3afc3-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="3afc3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="3afc3-108">Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää</span><span class="sxs-lookup"><span data-stu-id="3afc3-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="3afc3-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="3afc3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3afc3-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="3afc3-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3afc3-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="3afc3-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="3afc3-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="3afc3-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="3afc3-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="3afc3-113">Click Designer.</span></span>
6. <span data-ttu-id="3afc3-114">Valitse puussa "Customer invoice(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="3afc3-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="3afc3-115">Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="3afc3-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="3afc3-116">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="3afc3-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="3afc3-117">Kirjoita Nimi-kenttään "Laskun liitteet".</span><span class="sxs-lookup"><span data-stu-id="3afc3-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="3afc3-118">Laskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="3afc3-118">Invoice attachments</span></span>  
9. <span data-ttu-id="3afc3-119">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="3afc3-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="3afc3-120">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3afc3-120">Click Add.</span></span>
11. <span data-ttu-id="3afc3-121">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="3afc3-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="3afc3-122">Kirjoita Nimi-kenttään "Tiedostosisältö".</span><span class="sxs-lookup"><span data-stu-id="3afc3-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="3afc3-123">Tiedoston sisältö</span><span class="sxs-lookup"><span data-stu-id="3afc3-123">File content</span></span>  
13. <span data-ttu-id="3afc3-124">Valitse Nimiketyyppi-kenttään "Säilö".</span><span class="sxs-lookup"><span data-stu-id="3afc3-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="3afc3-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3afc3-125">Click Add.</span></span>
15. <span data-ttu-id="3afc3-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="3afc3-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="3afc3-127">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="3afc3-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="3afc3-128">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="3afc3-128">File name</span></span>  
17. <span data-ttu-id="3afc3-129">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="3afc3-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="3afc3-130">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3afc3-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="3afc3-131">Uusien tietomallielementtien yhdistäminen Dynamics 365 for Finance and Operations -sovelluksen tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="3afc3-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="3afc3-132">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="3afc3-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="3afc3-133">Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="3afc3-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="3afc3-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="3afc3-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="3afc3-135">Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="3afc3-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="3afc3-136">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="3afc3-136">Click Designer.</span></span>
4. <span data-ttu-id="3afc3-137">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="3afc3-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="3afc3-138">Laajenna puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="3afc3-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="3afc3-139">Valitse puussa solmu "Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="3afc3-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="3afc3-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3afc3-140">Click Edit.</span></span>
8. <span data-ttu-id="3afc3-141">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="3afc3-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="3afc3-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="3afc3-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="3afc3-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3afc3-143">Click Save.</span></span>
10. <span data-ttu-id="3afc3-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-144">Close the page.</span></span>
11. <span data-ttu-id="3afc3-145">Valitse puussa solmu "Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="3afc3-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="3afc3-146">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3afc3-146">Click Edit.</span></span>
13. <span data-ttu-id="3afc3-147">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="3afc3-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="3afc3-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="3afc3-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="3afc3-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3afc3-149">Click Save.</span></span>
15. <span data-ttu-id="3afc3-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-150">Close the page.</span></span>
16. <span data-ttu-id="3afc3-151">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="3afc3-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="3afc3-152">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3afc3-152">Click Edit.</span></span>
18. <span data-ttu-id="3afc3-153">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="3afc3-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="3afc3-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="3afc3-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="3afc3-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3afc3-155">Click Save.</span></span>
20. <span data-ttu-id="3afc3-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-156">Close the page.</span></span>
21. <span data-ttu-id="3afc3-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3afc3-157">Click Save.</span></span>
22. <span data-ttu-id="3afc3-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-158">Close the page.</span></span>
23. <span data-ttu-id="3afc3-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-159">Close the page.</span></span>
24. <span data-ttu-id="3afc3-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3afc3-160">Close the page.</span></span>
25. <span data-ttu-id="3afc3-161">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="3afc3-161">Click Change status.</span></span>
26. <span data-ttu-id="3afc3-162">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="3afc3-162">Click Complete.</span></span>
27. <span data-ttu-id="3afc3-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3afc3-163">Click OK.</span></span>


