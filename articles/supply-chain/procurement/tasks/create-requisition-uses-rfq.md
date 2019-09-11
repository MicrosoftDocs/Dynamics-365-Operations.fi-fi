---
title: Luo ehdotus, joka käyttää tarjouspyyntöä
description: Tässä aiheessa kerrotaan, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.
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
ms.openlocfilehash: 4429bda6efddbb4f1fa7da06e91e51d885919c05
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914951"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="c0714-103">Luo ehdotus, joka käyttää tarjouspyyntöä</span><span class="sxs-lookup"><span data-stu-id="c0714-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0714-104">Tässä aiheessa kerrotaan, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.</span><span class="sxs-lookup"><span data-stu-id="c0714-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="c0714-105">Tämän oppaan esimerkkiä voidaan käyttää USMF-yrityksen demotiedoilla, ja sinun on kirjauduttava järjestelmänvalvojana suorittaaksesi kaikki vaiheet.</span><span class="sxs-lookup"><span data-stu-id="c0714-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="c0714-106">Tässä oppaassa tehtävät kuuluvat yleensä hankintojen asiantuntijoille.</span><span class="sxs-lookup"><span data-stu-id="c0714-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="c0714-107">Luo ehdotus</span><span class="sxs-lookup"><span data-stu-id="c0714-107">Create a requisition</span></span>
1. <span data-ttu-id="c0714-108">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="c0714-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="c0714-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c0714-109">Select **New**.</span></span>
3. <span data-ttu-id="c0714-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0714-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c0714-111">Kirjoita päivämäärä **Vaadittu päivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0714-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="c0714-112">Kirjoita päivämäärä **Kirjauspäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0714-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="c0714-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0714-113">Select **OK**.</span></span>
7. <span data-ttu-id="c0714-114">Anna tai valitse **Syy**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c0714-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="c0714-115">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="c0714-115">Select **Add line**.</span></span>
9. <span data-ttu-id="c0714-116">Valitse **Hankintaluokka**-kenttään puussa oleva luokka ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0714-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="c0714-117">Kirjoita arvo **Tuotteen nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0714-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="c0714-118">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="c0714-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="c0714-119">Syötä tai valitse arvo **Yksikkö**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c0714-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="c0714-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c0714-120">Select **Save**.</span></span>
14. <span data-ttu-id="c0714-121">Avaa valintaikkuna valitsemalla **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="c0714-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="c0714-122">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="c0714-122">Select **Submit**.</span></span>
16. <span data-ttu-id="c0714-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-123">Close the page.</span></span>
17. <span data-ttu-id="c0714-124">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="c0714-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="c0714-125">Määritä työnkulkutehtävä uudelleen</span><span class="sxs-lookup"><span data-stu-id="c0714-125">Reassign a workflow task</span></span>
<span data-ttu-id="c0714-126">Seuraava tehtävä on luoda tarjouspyyntö toimittajien tuotetarjouksia varten.</span><span class="sxs-lookup"><span data-stu-id="c0714-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="c0714-127">USMF-esittelytiedoissa ostoehdotuksen työnkululle on määritetty sääntö, jos toimittajaa ei ole valittu tai rivin yksikköhinta on 0, tietylle työntekijälle määritetään tarjouspyynnön luomisen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="c0714-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="c0714-128">Voit jatkaa tämän oppaan seuraamista delegoimalla kyseisen tehtävän toiselle käyttäjälle (itsellesi).</span><span class="sxs-lookup"><span data-stu-id="c0714-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="c0714-129">Voit tehdä tämän vain, jos olet kirjautunut sisään järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="c0714-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="c0714-130">Avaa valintaikkuna valitsemalla **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="c0714-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="c0714-131">Valitse **Näytä historia**.</span><span class="sxs-lookup"><span data-stu-id="c0714-131">Select **View history**.</span></span>
3. <span data-ttu-id="c0714-132">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-132">Refresh the page.</span></span>
4. <span data-ttu-id="c0714-133">Laajenna **Seurantatiedot** -osa.</span><span class="sxs-lookup"><span data-stu-id="c0714-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="c0714-134">Valitse puusta rivi, joka alkaa "Rivin työnkulku käynnistetty".</span><span class="sxs-lookup"><span data-stu-id="c0714-134">In the tree, select the line that starts with “Line workflow activated on”.</span></span>
6. <span data-ttu-id="c0714-135">Valitse **Näytä työnkulun tiedot**.</span><span class="sxs-lookup"><span data-stu-id="c0714-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="c0714-136">Laajenna **Työnimikkeet**-osa.</span><span class="sxs-lookup"><span data-stu-id="c0714-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="c0714-137">Valitse **Määritä uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="c0714-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="c0714-138">Valitse **Järjestelmänvalvoja** **Käyttäjä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c0714-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="c0714-139">Valitse **Määritä uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="c0714-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="c0714-140">Sulje sivut.</span><span class="sxs-lookup"><span data-stu-id="c0714-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="c0714-141">Luo tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="c0714-141">Create an RFQ</span></span>

1. <span data-ttu-id="c0714-142">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-142">Refresh the page.</span></span>
2. <span data-ttu-id="c0714-143">Valitse **Tarjouspyyntö**.</span><span class="sxs-lookup"><span data-stu-id="c0714-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="c0714-144">Valitse **Ostava yritys** -kenttään **USMF**.</span><span class="sxs-lookup"><span data-stu-id="c0714-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="c0714-145">Valitse sama yritys, joka on ehdotusrivillä.</span><span class="sxs-lookup"><span data-stu-id="c0714-145">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="c0714-146">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c0714-146">In the list, mark the selected row.</span></span> <span data-ttu-id="c0714-147">Jos ostoehdotuksessa on useita rivejä, valitse kaikki rivit, jotka haluat lisätä tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="c0714-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="c0714-148">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0714-148">Select **OK**.</span></span>
6. <span data-ttu-id="c0714-149">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-149">Refresh the page.</span></span>
7. <span data-ttu-id="c0714-150">Varmista, että tietoruutu on avoinna ja laajenna **Liittyvät asiakirjat** -osa.</span><span class="sxs-lookup"><span data-stu-id="c0714-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="c0714-151">Valitse **Tarjouspyyntö**-kentän linkkiä avataksesi juuri luodun tarjouspyynnön.</span><span class="sxs-lookup"><span data-stu-id="c0714-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="c0714-152">Valitse **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="c0714-152">Select **Header**.</span></span>
10. <span data-ttu-id="c0714-153">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c0714-153">Select **Add**.</span></span>
11. <span data-ttu-id="c0714-154">Anna tai valitse arvo **Toimittajatili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c0714-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="c0714-155">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c0714-155">Select **Add**.</span></span>
13. <span data-ttu-id="c0714-156">Anna tai valitse arvo **Toimittajatili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c0714-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="c0714-157">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="c0714-157">Select **Send**.</span></span>
15. <span data-ttu-id="c0714-158">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0714-158">Select **OK**.</span></span>
16. <span data-ttu-id="c0714-159">Valitse **Kirjoita vastaus**.</span><span class="sxs-lookup"><span data-stu-id="c0714-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="c0714-160">Valitse toimintoruudussa **Vastaa**.</span><span class="sxs-lookup"><span data-stu-id="c0714-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="c0714-161">Valitse **Kopioi tiedot vastaukseen**.</span><span class="sxs-lookup"><span data-stu-id="c0714-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="c0714-162">Tämä kopioi tarjouspyynnön tiedot, kuten määrän ja päivämäärät, vastaukseen.</span><span class="sxs-lookup"><span data-stu-id="c0714-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="c0714-163">Syötä **Yksikköhinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c0714-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="c0714-164">Tämä on hinta, jonka olet saanut toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="c0714-164">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="c0714-165">Voit myös halutessasi kirjoittaa toimittajalta saamiasi lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="c0714-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="c0714-166">Valitse **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="c0714-166">Select **Accept**.</span></span>
21. <span data-ttu-id="c0714-167">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0714-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="c0714-168">Tarkista, että hinta ja toimittaja on siirretty ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="c0714-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="c0714-169">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-169">Close the page.</span></span>
2. <span data-ttu-id="c0714-170">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="c0714-170">Select **Lines**.</span></span>
3. <span data-ttu-id="c0714-171">Valitse **Aiheeseen liittyviä tietoja**.</span><span class="sxs-lookup"><span data-stu-id="c0714-171">Select **Related information**.</span></span>
4. <span data-ttu-id="c0714-172">Valitse **Ostoehdotus**.</span><span class="sxs-lookup"><span data-stu-id="c0714-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="c0714-173">Valitse tarjouspyyntöön siirretty rivi.</span><span class="sxs-lookup"><span data-stu-id="c0714-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="c0714-174">Tarkista, että hinta ja toimittaja on kopioitu ehdotukseen..</span><span class="sxs-lookup"><span data-stu-id="c0714-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="c0714-175">Avaa valintaikkuna valitsemalla **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="c0714-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="c0714-176">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="c0714-176">Select Complete.</span></span>
8. <span data-ttu-id="c0714-177">Valitse sivu.</span><span class="sxs-lookup"><span data-stu-id="c0714-177">Select the page.</span></span>
9. <span data-ttu-id="c0714-178">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="c0714-178">Select Complete.</span></span>

