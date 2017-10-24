--- 
title: "Tietomallin laajentaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f3d494cc83b273eef071b23d0948b283ba85c17e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="f95f0-103">Tietomallin laajentaminen tiedostonhallinnan tiedostojen käyttämiseksi muodon tuotoksissa sähköistä raportointia (ER) varten</span><span class="sxs-lookup"><span data-stu-id="f95f0-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f95f0-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon käyttämään tiedostonhallinnan tiedostoja (liitetiedostot) ER-tuotoksissa.</span><span class="sxs-lookup"><span data-stu-id="f95f0-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f95f0-105">Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="f95f0-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f95f0-106">Jotta voisit suorittaa nämä toimet, sinun on ensin suoritettava "ER Käytä tiedostojen hallinta tiedostojen muotoa tulosteissa (osa 1: valmistele tietomalli)" -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f95f0-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="f95f0-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="f95f0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="f95f0-108">Laajentaa tietomallia niin, sen sisältämät tiedostonhallinnan tiedostot voi esittää</span><span class="sxs-lookup"><span data-stu-id="f95f0-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="f95f0-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="f95f0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f95f0-110">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="f95f0-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f95f0-111">Laajenna puussa solmu "Customer invoice model".</span><span class="sxs-lookup"><span data-stu-id="f95f0-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="f95f0-112">Valitse puusta "Customer invoice model\Customer invoice model (custom)".</span><span class="sxs-lookup"><span data-stu-id="f95f0-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="f95f0-113">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f95f0-113">Click Designer.</span></span>
6. <span data-ttu-id="f95f0-114">Valitse puussa "Customer invoice(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="f95f0-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="f95f0-115">Tätä tietomallia laajennetaan, jotta sitä voi käyttää kaikissa tiedostoissa, jotka on liitetty myyntitilaukseen, joka liittyy sähköisesti käsiteltävään laskuun.</span><span class="sxs-lookup"><span data-stu-id="f95f0-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="f95f0-116">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f95f0-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f95f0-117">Kirjoita Nimi-kenttään "Laskun liitteet".</span><span class="sxs-lookup"><span data-stu-id="f95f0-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="f95f0-118">Laskujen liitteet</span><span class="sxs-lookup"><span data-stu-id="f95f0-118">Invoice attachments</span></span>  
9. <span data-ttu-id="f95f0-119">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="f95f0-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="f95f0-120">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f95f0-120">Click Add.</span></span>
11. <span data-ttu-id="f95f0-121">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f95f0-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="f95f0-122">Kirjoita Nimi-kenttään "Tiedostosisältö".</span><span class="sxs-lookup"><span data-stu-id="f95f0-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="f95f0-123">Tiedoston sisältö</span><span class="sxs-lookup"><span data-stu-id="f95f0-123">File content</span></span>  
13. <span data-ttu-id="f95f0-124">Valitse Nimiketyyppi-kenttään "Säilö".</span><span class="sxs-lookup"><span data-stu-id="f95f0-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="f95f0-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f95f0-125">Click Add.</span></span>
15. <span data-ttu-id="f95f0-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f95f0-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="f95f0-127">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="f95f0-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="f95f0-128">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="f95f0-128">File name</span></span>  
17. <span data-ttu-id="f95f0-129">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="f95f0-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="f95f0-130">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f95f0-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="f95f0-131">Uusien tietomallielementtien yhdistäminen Dynamics 365 for Finance and Operations, Enterprise editionin tietolähteisiin</span><span class="sxs-lookup"><span data-stu-id="f95f0-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="f95f0-132">Valitse Yhdistä malli tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="f95f0-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="f95f0-133">Pikasuodattimen avulla voit suodattaa Määritys-kentän arvolla "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="f95f0-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="f95f0-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="f95f0-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="f95f0-135">Yhdistä uuden mallin elementit asianmukaisiin tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="f95f0-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="f95f0-136">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f95f0-136">Click Designer.</span></span>
4. <span data-ttu-id="f95f0-137">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="f95f0-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="f95f0-138">Laajenna puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="f95f0-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="f95f0-139">Valitse puussa solmu "Invoice attachments\File name".</span><span class="sxs-lookup"><span data-stu-id="f95f0-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="f95f0-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="f95f0-140">Click Edit.</span></span>
8. <span data-ttu-id="f95f0-141">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="f95f0-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="f95f0-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="f95f0-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="f95f0-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f95f0-143">Click Save.</span></span>
10. <span data-ttu-id="f95f0-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-144">Close the page.</span></span>
11. <span data-ttu-id="f95f0-145">Valitse puussa solmu "Invoice attachments\File content".</span><span class="sxs-lookup"><span data-stu-id="f95f0-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="f95f0-146">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="f95f0-146">Click Edit.</span></span>
13. <span data-ttu-id="f95f0-147">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="f95f0-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="f95f0-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="f95f0-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="f95f0-149">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f95f0-149">Click Save.</span></span>
15. <span data-ttu-id="f95f0-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-150">Close the page.</span></span>
16. <span data-ttu-id="f95f0-151">Valitse puussa solmu "Invoice attachments".</span><span class="sxs-lookup"><span data-stu-id="f95f0-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="f95f0-152">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="f95f0-152">Click Edit.</span></span>
18. <span data-ttu-id="f95f0-153">Kirjoita Kaava-kenttään 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="f95f0-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="f95f0-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="f95f0-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="f95f0-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f95f0-155">Click Save.</span></span>
20. <span data-ttu-id="f95f0-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-156">Close the page.</span></span>
21. <span data-ttu-id="f95f0-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f95f0-157">Click Save.</span></span>
22. <span data-ttu-id="f95f0-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-158">Close the page.</span></span>
23. <span data-ttu-id="f95f0-159">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-159">Close the page.</span></span>
24. <span data-ttu-id="f95f0-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95f0-160">Close the page.</span></span>
25. <span data-ttu-id="f95f0-161">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="f95f0-161">Click Change status.</span></span>
26. <span data-ttu-id="f95f0-162">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="f95f0-162">Click Complete.</span></span>
27. <span data-ttu-id="f95f0-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f95f0-163">Click OK.</span></span>


