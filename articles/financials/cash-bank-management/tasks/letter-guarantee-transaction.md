---
title: Takausasiakirjan tapahtuma
description: Tässä menettelyssä käsitellään takuuasiakirjaprosessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566107"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="f8154-103">Takausasiakirjan tapahtuma</span><span class="sxs-lookup"><span data-stu-id="f8154-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8154-104">Tässä menettelyssä käsitellään takuuasiakirjaprosessi.</span><span class="sxs-lookup"><span data-stu-id="f8154-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="f8154-105">Seuraavat tehtävät on suoritettava, ennen kuin tämä menettely tehdään:</span><span class="sxs-lookup"><span data-stu-id="f8154-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="f8154-106">Määritä pankin limiitit ja kirjausprofiilit takauskirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="f8154-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="f8154-107">Luo pankin limiittisopimus takausasiakirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="f8154-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="f8154-108">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f8154-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="f8154-109">Luo myyntitilaus, jossa on takausasiakirja</span><span class="sxs-lookup"><span data-stu-id="f8154-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="f8154-110">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="f8154-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f8154-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f8154-111">Click New.</span></span>
3. <span data-ttu-id="f8154-112">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f8154-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="f8154-113">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-113">Expand the General section.</span></span>
5. <span data-ttu-id="f8154-114">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f8154-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f8154-116">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f8154-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="f8154-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f8154-118">Valitse Pankkitositteen tyyppi -kentässä Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="f8154-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-119">Click OK.</span></span>
11. <span data-ttu-id="f8154-120">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f8154-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f8154-121">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f8154-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="f8154-122">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="f8154-123">Valitse Toimitus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f8154-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="f8154-124">Huomautus: Valitse Toimituspäivän tarkistus = Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="f8154-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="f8154-125">Kirjoita päivämäärä Pyydetty lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="f8154-126">Kirjoita päivämäärä Vahvistettu lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="f8154-127">Käsittele takausasiakirja_Pyyntö</span><span class="sxs-lookup"><span data-stu-id="f8154-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="f8154-128">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="f8154-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="f8154-129">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="f8154-130">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="f8154-131">Avaa valintaikkuna valitsemalla Pyyntö.</span><span class="sxs-lookup"><span data-stu-id="f8154-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="f8154-132">Anna tai valitse Tyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f8154-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="f8154-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f8154-134">Kirjoita numero Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="f8154-135">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="f8154-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-136">Click OK.</span></span>
10. <span data-ttu-id="f8154-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8154-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="f8154-138">Käsittele takausasiakirja_Lähetä pankille</span><span class="sxs-lookup"><span data-stu-id="f8154-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="f8154-139">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="f8154-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="f8154-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f8154-141">Avaa valintaikkuna valitsemalla Lähetä pankille.</span><span class="sxs-lookup"><span data-stu-id="f8154-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="f8154-142">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f8154-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="f8154-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f8154-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="f8154-145">Käsittele takausasiakirja_Ota vastaan pankista</span><span class="sxs-lookup"><span data-stu-id="f8154-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="f8154-146">Avaa valintaikkuna valitsemalla Vastaanota pankilta.</span><span class="sxs-lookup"><span data-stu-id="f8154-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="f8154-147">Kirjoita arvo Pankin rekisteröintinumero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f8154-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="f8154-148">Tarkista Kate- ja Kulu-kentissä lasketut arvot.</span><span class="sxs-lookup"><span data-stu-id="f8154-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="f8154-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-149">Click OK.</span></span>
4. <span data-ttu-id="f8154-150">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="f8154-151">Tarkista Vastaanota pankilta -tietue.</span><span class="sxs-lookup"><span data-stu-id="f8154-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="f8154-152">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="f8154-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="f8154-153">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="f8154-153">Click Lines.</span></span>
    * <span data-ttu-id="f8154-154">Tarkista kirjauskansiovientien kirjaus.</span><span class="sxs-lookup"><span data-stu-id="f8154-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="f8154-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8154-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="f8154-156">Käsittele takausasiakirja_Anna edunsaajalle</span><span class="sxs-lookup"><span data-stu-id="f8154-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="f8154-157">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="f8154-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f8154-158">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f8154-159">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="f8154-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f8154-160">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f8154-161">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f8154-162">Avaa valintaikkuna valitsemalla Anna edunsaajalle.</span><span class="sxs-lookup"><span data-stu-id="f8154-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="f8154-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-163">Click OK.</span></span>
8. <span data-ttu-id="f8154-164">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="f8154-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f8154-165">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f8154-166">Avaa valintaikkuna valitsemalla Anna edunsaajalle.</span><span class="sxs-lookup"><span data-stu-id="f8154-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="f8154-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-167">Click OK.</span></span>
12. <span data-ttu-id="f8154-168">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="f8154-169">Vahvista Anna edunsaajalle -tietue.</span><span class="sxs-lookup"><span data-stu-id="f8154-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="f8154-170">Käsittele takausasiakirja_Kasvata arvoa</span><span class="sxs-lookup"><span data-stu-id="f8154-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="f8154-171">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="f8154-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f8154-172">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f8154-173">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="f8154-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f8154-174">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f8154-175">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f8154-176">Avaa valintaikkuna valitsemalla Kasvata arvoa.</span><span class="sxs-lookup"><span data-stu-id="f8154-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="f8154-177">Lisää Lisättävä arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f8154-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="f8154-178">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-178">Click OK.</span></span>
9. <span data-ttu-id="f8154-179">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="f8154-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="f8154-180">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f8154-181">Avaa valintaikkuna valitsemalla Kasvata arvoa.</span><span class="sxs-lookup"><span data-stu-id="f8154-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="f8154-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-182">Click OK.</span></span>
13. <span data-ttu-id="f8154-183">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="f8154-184">Tarkista Kasvata arvoa -tietue.</span><span class="sxs-lookup"><span data-stu-id="f8154-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="f8154-185">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f8154-186">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="f8154-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="f8154-187">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="f8154-187">Click Lines.</span></span>
    * <span data-ttu-id="f8154-188">Tarkista kirjatut kirjauskansioviennit.</span><span class="sxs-lookup"><span data-stu-id="f8154-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="f8154-189">Käsittele takausasiakirja_Realisoi</span><span class="sxs-lookup"><span data-stu-id="f8154-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="f8154-190">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="f8154-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f8154-191">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f8154-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f8154-192">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="f8154-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f8154-193">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f8154-194">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="f8154-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f8154-195">Avaa valintaikkuna valitsemalla Realisoi.</span><span class="sxs-lookup"><span data-stu-id="f8154-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="f8154-196">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-196">Click OK.</span></span>
8. <span data-ttu-id="f8154-197">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="f8154-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f8154-198">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f8154-199">Avaa valintaikkuna valitsemalla Realisoi.</span><span class="sxs-lookup"><span data-stu-id="f8154-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="f8154-200">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8154-200">Click OK.</span></span>
12. <span data-ttu-id="f8154-201">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="f8154-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="f8154-202">Tarkista Realisoi-tietue.</span><span class="sxs-lookup"><span data-stu-id="f8154-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="f8154-203">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f8154-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f8154-204">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="f8154-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="f8154-205">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="f8154-205">Click Lines.</span></span>
    * <span data-ttu-id="f8154-206">Tarkista kirjatut kirjauskansioviennit.</span><span class="sxs-lookup"><span data-stu-id="f8154-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="f8154-207">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8154-207">Close the page.</span></span>

