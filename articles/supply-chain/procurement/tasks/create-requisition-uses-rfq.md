---
title: Luo ehdotus, joka käyttää tarjouspyyntöä
description: Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d80f84c148ff26bf008a97b06098bfd18c9062d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844150"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="0f8b9-103">Luo ehdotus, joka käyttää tarjouspyyntöä</span><span class="sxs-lookup"><span data-stu-id="0f8b9-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f8b9-104">Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="0f8b9-105">Tämän oppaan esimerkkiä voidaan käyttää USMF-yrityksen demotiedoilla, ja sinun on kirjauduttava järjestelmänvalvojana suorittaaksesi kaikki vaiheet.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="0f8b9-106">Tässä oppaassa tehtävät kuuluvat yleensä hankintojen asiantuntijoille.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="0f8b9-107">Luo ehdotus</span><span class="sxs-lookup"><span data-stu-id="0f8b9-107">Create a requisition</span></span>
1. <span data-ttu-id="0f8b9-108">Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="0f8b9-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-109">Click New.</span></span>
3. <span data-ttu-id="0f8b9-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0f8b9-111">Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="0f8b9-112">Kirjoita päivämäärä Kirjauspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="0f8b9-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-113">Click OK.</span></span>
7. <span data-ttu-id="0f8b9-114">Anna tai valitse Syy-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="0f8b9-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-115">Click Add line.</span></span>
9. <span data-ttu-id="0f8b9-116">Valitse Hankintaluokka-kenttään puussa oleva luokka ja valitse sitten OK.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="0f8b9-117">Kirjoita arvo Tuotteen nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="0f8b9-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="0f8b9-119">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="0f8b9-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-120">Click Save.</span></span>
14. <span data-ttu-id="0f8b9-121">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="0f8b9-122">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-122">Click Submit.</span></span>
16. <span data-ttu-id="0f8b9-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-123">Close the page.</span></span>
17. <span data-ttu-id="0f8b9-124">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="0f8b9-125">Määritä työnkulkutehtävä uudelleen</span><span class="sxs-lookup"><span data-stu-id="0f8b9-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="0f8b9-126">Seuraava tehtävä on luoda tarjouspyyntö toimittajien tuotetarjouksia varten.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="0f8b9-127">USMF-esittelytiedoissa ostoehdotuksen työnkululle on määritetty sääntö, jos toimittajaa ei ole valittu tai rivin yksikköhinta on 0, tietylle työntekijälle määritetään tarjouspyynnön luomisen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="0f8b9-128">Voit jatkaa tämän oppaan seuraamista delegoimalla kyseisen tehtävän toiselle käyttäjälle (itsellesi).</span><span class="sxs-lookup"><span data-stu-id="0f8b9-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="0f8b9-129">Voit tehdä tämän vain, jos olet kirjautunut sisään järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="0f8b9-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="0f8b9-130">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="0f8b9-131">Valitse Näytä historia.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-131">Click View history.</span></span>
3. <span data-ttu-id="0f8b9-132">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-132">Refresh the page.</span></span>
4. <span data-ttu-id="0f8b9-133">Laajenna Seurantatiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="0f8b9-134">Valitse puusta "rivi, joka alkaa 'Rivin työnkulku käynnistetty'".</span><span class="sxs-lookup"><span data-stu-id="0f8b9-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="0f8b9-135">Valitse Näytä työnkulun tiedot.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-135">Click View workflow details.</span></span>
7. <span data-ttu-id="0f8b9-136">Laajenna Työnimikkeet-osa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="0f8b9-137">Valitse Määritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-137">Click Reassign.</span></span>
9. <span data-ttu-id="0f8b9-138">Valitse Järjestelmänvalvoja Käyttäjä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="0f8b9-139">Valitse Määritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-139">Click Reassign.</span></span>
11. <span data-ttu-id="0f8b9-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-140">Close the page.</span></span>
12. <span data-ttu-id="0f8b9-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="0f8b9-142">Luo tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="0f8b9-142">Create an RFQ</span></span>
1. <span data-ttu-id="0f8b9-143">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-143">Refresh the page.</span></span>
2. <span data-ttu-id="0f8b9-144">Valitse Tarjouspyynnön vastaus.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="0f8b9-145">Valitse Ostava yritys -kenttään USMF.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="0f8b9-146">Valitse sama yritys, joka on ehdotusrivillä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="0f8b9-147">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0f8b9-148">Jos ostoehdotuksessa on useita rivejä, valitse kaikki rivit, jotka haluat lisätä tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="0f8b9-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-149">Click OK.</span></span>
6. <span data-ttu-id="0f8b9-150">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-150">Refresh the page.</span></span>
7. <span data-ttu-id="0f8b9-151">Avaa tietoruutu ja laajenna liittyvien asiakirjojen osa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="0f8b9-152">Tietoruutu saattaa olla jo auki.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-152">You may already have the FactBox open.</span></span> <span data-ttu-id="0f8b9-153">Paikanna nuolikuvake, joka on Rivit-/Otsikko-vaihtopainikkeen oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="0f8b9-154">Jos nuoli osoittaa oikealle, tietoruudun on jo avoinna.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="0f8b9-155">Vasemmalle osoittavasta nuolesta saat avattua tietoruudun.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="0f8b9-156">Napsauta Tarjouspyyntö-kentän linkkiä avataksesi juuri luodun tarjouspyynnön.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="0f8b9-157">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-157">Click Header.</span></span>
10. <span data-ttu-id="0f8b9-158">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-158">Click Add.</span></span>
11. <span data-ttu-id="0f8b9-159">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="0f8b9-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-160">Click Add.</span></span>
13. <span data-ttu-id="0f8b9-161">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="0f8b9-162">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-162">Click Send.</span></span>
15. <span data-ttu-id="0f8b9-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-163">Click OK.</span></span>
16. <span data-ttu-id="0f8b9-164">Napsauta Kirjoita vastaus -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-164">Click Enter reply.</span></span>
17. <span data-ttu-id="0f8b9-165">Valitse toimintoruudussa Vastaa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="0f8b9-166">Napsauta Kopioi tiedot vastauskenttiin -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="0f8b9-167">Tämä kopioi tarjouspyynnön tiedot, kuten määrän ja päivämäärät, vastaukseen.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="0f8b9-168">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="0f8b9-169">Tämä on hinta, jonka olet saanut toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="0f8b9-170">Voit myös halutessasi kirjoittaa toimittajalta saamiasi lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="0f8b9-171">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-171">Click Accept.</span></span>
21. <span data-ttu-id="0f8b9-172">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="0f8b9-173">Tarkista, että hinta ja toimittaja on siirretty ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="0f8b9-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="0f8b9-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-174">Close the page.</span></span>
2. <span data-ttu-id="0f8b9-175">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-175">Click Lines.</span></span>
3. <span data-ttu-id="0f8b9-176">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-176">Click Related information.</span></span>
4. <span data-ttu-id="0f8b9-177">Valitse Ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="0f8b9-178">Valitse tarjouspyyntöön siirretty rivi.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="0f8b9-179">Tarkista, että hinta ja toimittaja on kopioitu ehdotukseen..</span><span class="sxs-lookup"><span data-stu-id="0f8b9-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="0f8b9-180">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="0f8b9-181">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-181">Click Complete.</span></span>
8. <span data-ttu-id="0f8b9-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-182">Close the page.</span></span>
9. <span data-ttu-id="0f8b9-183">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="0f8b9-183">Click Complete.</span></span>

