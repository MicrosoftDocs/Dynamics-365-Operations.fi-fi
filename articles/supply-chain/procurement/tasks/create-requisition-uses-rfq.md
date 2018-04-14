--- 
title: "Luo ehdotus, joka käyttää tarjouspyyntöä"
description: "Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2c2daad961ec5c47ca49b2e53a2118570caf6a58
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="dcd17-103">Luo ehdotus, joka käyttää tarjouspyyntöä</span><span class="sxs-lookup"><span data-stu-id="dcd17-103">Create a requisition that uses an RFQ</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcd17-104">Tässä oppaassa esitellään, miten hinta- ja toimittajatiedot lisätään ostoehdotukseen tarjouspyyntöprosessista.</span><span class="sxs-lookup"><span data-stu-id="dcd17-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="dcd17-105">Tämän oppaan esimerkkiä voidaan käyttää USMF-yrityksen demotiedoilla, ja sinun on kirjauduttava järjestelmänvalvojana suorittaaksesi kaikki vaiheet.</span><span class="sxs-lookup"><span data-stu-id="dcd17-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="dcd17-106">Tässä oppaassa tehtävät kuuluvat yleensä hankintojen asiantuntijoille.</span><span class="sxs-lookup"><span data-stu-id="dcd17-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="dcd17-107">Luo ehdotus</span><span class="sxs-lookup"><span data-stu-id="dcd17-107">Create a requisition</span></span>
1. <span data-ttu-id="dcd17-108">Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="dcd17-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="dcd17-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dcd17-109">Click New.</span></span>
3. <span data-ttu-id="dcd17-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dcd17-111">Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="dcd17-112">Kirjoita päivämäärä Kirjauspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="dcd17-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcd17-113">Click OK.</span></span>
7. <span data-ttu-id="dcd17-114">Anna tai valitse Syy-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dcd17-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="dcd17-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="dcd17-115">Click Add line.</span></span>
9. <span data-ttu-id="dcd17-116">Valitse Hankintaluokka-kenttään puussa oleva luokka ja valitse sitten OK.</span><span class="sxs-lookup"><span data-stu-id="dcd17-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="dcd17-117">Kirjoita arvo Tuotteen nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="dcd17-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="dcd17-119">Syötä tai valitse arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcd17-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="dcd17-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="dcd17-120">Click Save.</span></span>
14. <span data-ttu-id="dcd17-121">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="dcd17-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="dcd17-122">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-122">Click Submit.</span></span>
16. <span data-ttu-id="dcd17-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-123">Close the page.</span></span>
17. <span data-ttu-id="dcd17-124">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="dcd17-125">Määritä työnkulkutehtävä uudelleen</span><span class="sxs-lookup"><span data-stu-id="dcd17-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="dcd17-126">Seuraava tehtävä on luoda tarjouspyyntö toimittajien tuotetarjouksia varten.</span><span class="sxs-lookup"><span data-stu-id="dcd17-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="dcd17-127">USMF-esittelytiedoissa ostoehdotuksen työnkululle on määritetty sääntö, jos toimittajaa ei ole valittu tai rivin yksikköhinta on 0, tietylle työntekijälle määritetään tarjouspyynnön luomisen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="dcd17-128">Voit jatkaa tämän oppaan seuraamista delegoimalla kyseisen tehtävän toiselle käyttäjälle (itsellesi).</span><span class="sxs-lookup"><span data-stu-id="dcd17-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="dcd17-129">Voit tehdä tämän vain, jos olet kirjautunut sisään järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="dcd17-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="dcd17-130">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="dcd17-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="dcd17-131">Valitse Näytä historia.</span><span class="sxs-lookup"><span data-stu-id="dcd17-131">Click View history.</span></span>
3. <span data-ttu-id="dcd17-132">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-132">Refresh the page.</span></span>
4. <span data-ttu-id="dcd17-133">Laajenna Seurantatiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="dcd17-134">Valitse puusta "rivi, joka alkaa 'Rivin työnkulku käynnistetty'".</span><span class="sxs-lookup"><span data-stu-id="dcd17-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="dcd17-135">Valitse Näytä työnkulun tiedot.</span><span class="sxs-lookup"><span data-stu-id="dcd17-135">Click View workflow details.</span></span>
7. <span data-ttu-id="dcd17-136">Laajenna Työnimikkeet-osa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="dcd17-137">Valitse Määritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="dcd17-137">Click Reassign.</span></span>
9. <span data-ttu-id="dcd17-138">Valitse Järjestelmänvalvoja Käyttäjä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="dcd17-139">Valitse Määritä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="dcd17-139">Click Reassign.</span></span>
11. <span data-ttu-id="dcd17-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-140">Close the page.</span></span>
12. <span data-ttu-id="dcd17-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="dcd17-142">Luo tarjouspyyntö</span><span class="sxs-lookup"><span data-stu-id="dcd17-142">Create an RFQ</span></span>
1. <span data-ttu-id="dcd17-143">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-143">Refresh the page.</span></span>
2. <span data-ttu-id="dcd17-144">Valitse Tarjouspyynnön vastaus.</span><span class="sxs-lookup"><span data-stu-id="dcd17-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="dcd17-145">Valitse Ostava yritys -kenttään USMF.</span><span class="sxs-lookup"><span data-stu-id="dcd17-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="dcd17-146">Valitse sama yritys, joka on ehdotusrivillä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="dcd17-147">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dcd17-148">Jos ostoehdotuksessa on useita rivejä, valitse kaikki rivit, jotka haluat lisätä tarjouspyyntöön.</span><span class="sxs-lookup"><span data-stu-id="dcd17-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="dcd17-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcd17-149">Click OK.</span></span>
6. <span data-ttu-id="dcd17-150">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-150">Refresh the page.</span></span>
7. <span data-ttu-id="dcd17-151">Avaa tietoruutu ja laajenna liittyvien asiakirjojen osa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="dcd17-152">Tietoruutu saattaa olla jo auki.</span><span class="sxs-lookup"><span data-stu-id="dcd17-152">You may already have the FactBox open.</span></span> <span data-ttu-id="dcd17-153">Paikanna nuolikuvake, joka on Rivit-/Otsikko-vaihtopainikkeen oikealla puolella.</span><span class="sxs-lookup"><span data-stu-id="dcd17-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="dcd17-154">Jos nuoli osoittaa oikealle, tietoruudun on jo avoinna.</span><span class="sxs-lookup"><span data-stu-id="dcd17-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="dcd17-155">Vasemmalle osoittavasta nuolesta saat avattua tietoruudun.</span><span class="sxs-lookup"><span data-stu-id="dcd17-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="dcd17-156">Napsauta Tarjouspyyntö-kentän linkkiä avataksesi juuri luodun tarjouspyynnön.</span><span class="sxs-lookup"><span data-stu-id="dcd17-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="dcd17-157">Napsauta otsikkoa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-157">Click Header.</span></span>
10. <span data-ttu-id="dcd17-158">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="dcd17-158">Click Add.</span></span>
11. <span data-ttu-id="dcd17-159">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="dcd17-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="dcd17-160">Click Add.</span></span>
13. <span data-ttu-id="dcd17-161">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="dcd17-162">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="dcd17-162">Click Send.</span></span>
15. <span data-ttu-id="dcd17-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcd17-163">Click OK.</span></span>
16. <span data-ttu-id="dcd17-164">Napsauta Kirjoita vastaus -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-164">Click Enter reply.</span></span>
17. <span data-ttu-id="dcd17-165">Valitse toimintoruudussa Vastaa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="dcd17-166">Napsauta Kopioi tiedot vastauskenttiin -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="dcd17-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="dcd17-167">Tämä kopioi tarjouspyynnön tiedot, kuten määrän ja päivämäärät, vastaukseen.</span><span class="sxs-lookup"><span data-stu-id="dcd17-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="dcd17-168">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="dcd17-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="dcd17-169">Tämä on hinta, jonka olet saanut toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="dcd17-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="dcd17-170">Voit myös halutessasi kirjoittaa toimittajalta saamiasi lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="dcd17-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="dcd17-171">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="dcd17-171">Click Accept.</span></span>
21. <span data-ttu-id="dcd17-172">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcd17-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="dcd17-173">Tarkista, että hinta ja toimittaja on siirretty ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="dcd17-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="dcd17-174">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-174">Close the page.</span></span>
2. <span data-ttu-id="dcd17-175">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="dcd17-175">Click Lines.</span></span>
3. <span data-ttu-id="dcd17-176">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="dcd17-176">Click Related information.</span></span>
4. <span data-ttu-id="dcd17-177">Valitse Ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="dcd17-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="dcd17-178">Valitse tarjouspyyntöön siirretty rivi.</span><span class="sxs-lookup"><span data-stu-id="dcd17-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="dcd17-179">Tarkista, että hinta ja toimittaja on kopioitu ehdotukseen..</span><span class="sxs-lookup"><span data-stu-id="dcd17-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="dcd17-180">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="dcd17-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="dcd17-181">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="dcd17-181">Click Complete.</span></span>
8. <span data-ttu-id="dcd17-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcd17-182">Close the page.</span></span>
9. <span data-ttu-id="dcd17-183">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="dcd17-183">Click Complete.</span></span>


