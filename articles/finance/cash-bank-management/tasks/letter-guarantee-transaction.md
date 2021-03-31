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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566849cfcedd29f4bb92d08a17b67e16b1cbc372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225366"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="46eaa-103">Takausasiakirjan tapahtuma</span><span class="sxs-lookup"><span data-stu-id="46eaa-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46eaa-104">Tässä menettelyssä käsitellään takuuasiakirjaprosessi.</span><span class="sxs-lookup"><span data-stu-id="46eaa-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="46eaa-105">Seuraavat tehtävät on suoritettava, ennen kuin tämä menettely tehdään:</span><span class="sxs-lookup"><span data-stu-id="46eaa-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="46eaa-106">Määritä pankin limiitit ja kirjausprofiilit takauskirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="46eaa-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="46eaa-107">Luo pankin limiittisopimus takausasiakirjaa varten.</span><span class="sxs-lookup"><span data-stu-id="46eaa-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="46eaa-108">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="46eaa-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="46eaa-109">Luo myyntitilaus, jossa on takausasiakirja</span><span class="sxs-lookup"><span data-stu-id="46eaa-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="46eaa-110">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="46eaa-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="46eaa-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="46eaa-111">Click New.</span></span>
3. <span data-ttu-id="46eaa-112">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="46eaa-113">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-113">Expand the General section.</span></span>
5. <span data-ttu-id="46eaa-114">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="46eaa-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="46eaa-116">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="46eaa-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="46eaa-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46eaa-118">Valitse Pankkitositteen tyyppi -kentässä Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="46eaa-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-119">Click OK.</span></span>
11. <span data-ttu-id="46eaa-120">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="46eaa-121">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46eaa-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="46eaa-122">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="46eaa-123">Valitse Toimitus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="46eaa-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="46eaa-124">Huomautus: Valitse Toimituspäivän tarkistus = Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="46eaa-125">Kirjoita päivämäärä Pyydetty lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="46eaa-126">Kirjoita päivämäärä Vahvistettu lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="46eaa-127">Käsittele takausasiakirja_Pyyntö</span><span class="sxs-lookup"><span data-stu-id="46eaa-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="46eaa-128">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="46eaa-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="46eaa-129">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="46eaa-130">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="46eaa-131">Avaa valintaikkuna valitsemalla Pyyntö.</span><span class="sxs-lookup"><span data-stu-id="46eaa-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="46eaa-132">Anna tai valitse Tyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="46eaa-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="46eaa-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="46eaa-134">Kirjoita numero Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="46eaa-135">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="46eaa-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-136">Click OK.</span></span>
10. <span data-ttu-id="46eaa-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46eaa-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="46eaa-138">Käsittele takausasiakirja_Lähetä pankille</span><span class="sxs-lookup"><span data-stu-id="46eaa-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="46eaa-139">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="46eaa-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="46eaa-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46eaa-141">Avaa valintaikkuna valitsemalla Lähetä pankille.</span><span class="sxs-lookup"><span data-stu-id="46eaa-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="46eaa-142">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="46eaa-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="46eaa-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="46eaa-145">Käsittele takausasiakirja_Ota vastaan pankista</span><span class="sxs-lookup"><span data-stu-id="46eaa-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="46eaa-146">Avaa valintaikkuna valitsemalla Vastaanota pankilta.</span><span class="sxs-lookup"><span data-stu-id="46eaa-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="46eaa-147">Kirjoita arvo Pankin rekisteröintinumero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="46eaa-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="46eaa-148">Tarkista Kate- ja Kulu-kentissä lasketut arvot.</span><span class="sxs-lookup"><span data-stu-id="46eaa-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="46eaa-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-149">Click OK.</span></span>
4. <span data-ttu-id="46eaa-150">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="46eaa-151">Tarkista Vastaanota pankilta -tietue.</span><span class="sxs-lookup"><span data-stu-id="46eaa-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="46eaa-152">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="46eaa-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="46eaa-153">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="46eaa-153">Click Lines.</span></span>
    * <span data-ttu-id="46eaa-154">Tarkista kirjauskansiovientien kirjaus.</span><span class="sxs-lookup"><span data-stu-id="46eaa-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="46eaa-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46eaa-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="46eaa-156">Käsittele takausasiakirja_Anna edunsaajalle</span><span class="sxs-lookup"><span data-stu-id="46eaa-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="46eaa-157">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="46eaa-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="46eaa-158">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="46eaa-159">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="46eaa-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="46eaa-160">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="46eaa-161">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="46eaa-162">Avaa valintaikkuna valitsemalla Anna edunsaajalle.</span><span class="sxs-lookup"><span data-stu-id="46eaa-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="46eaa-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-163">Click OK.</span></span>
8. <span data-ttu-id="46eaa-164">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="46eaa-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="46eaa-165">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="46eaa-166">Avaa valintaikkuna valitsemalla Anna edunsaajalle.</span><span class="sxs-lookup"><span data-stu-id="46eaa-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="46eaa-167">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-167">Click OK.</span></span>
12. <span data-ttu-id="46eaa-168">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="46eaa-169">Vahvista Anna edunsaajalle -tietue.</span><span class="sxs-lookup"><span data-stu-id="46eaa-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="46eaa-170">Käsittele takausasiakirja_Kasvata arvoa</span><span class="sxs-lookup"><span data-stu-id="46eaa-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="46eaa-171">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="46eaa-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="46eaa-172">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="46eaa-173">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="46eaa-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="46eaa-174">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="46eaa-175">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="46eaa-176">Avaa valintaikkuna valitsemalla Kasvata arvoa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="46eaa-177">Lisää Lisättävä arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="46eaa-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="46eaa-178">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-178">Click OK.</span></span>
9. <span data-ttu-id="46eaa-179">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="46eaa-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="46eaa-180">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="46eaa-181">Avaa valintaikkuna valitsemalla Kasvata arvoa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="46eaa-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-182">Click OK.</span></span>
13. <span data-ttu-id="46eaa-183">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="46eaa-184">Tarkista Kasvata arvoa -tietue.</span><span class="sxs-lookup"><span data-stu-id="46eaa-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="46eaa-185">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="46eaa-186">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="46eaa-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="46eaa-187">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="46eaa-187">Click Lines.</span></span>
    * <span data-ttu-id="46eaa-188">Tarkista kirjatut kirjauskansioviennit.</span><span class="sxs-lookup"><span data-stu-id="46eaa-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="46eaa-189">Käsittele takausasiakirja_Realisoi</span><span class="sxs-lookup"><span data-stu-id="46eaa-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="46eaa-190">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="46eaa-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="46eaa-191">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="46eaa-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="46eaa-192">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="46eaa-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="46eaa-193">Valitse Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="46eaa-194">Valitse toimintoruudussa Takausasiakirja.</span><span class="sxs-lookup"><span data-stu-id="46eaa-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="46eaa-195">Avaa valintaikkuna valitsemalla Realisoi.</span><span class="sxs-lookup"><span data-stu-id="46eaa-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="46eaa-196">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-196">Click OK.</span></span>
8. <span data-ttu-id="46eaa-197">Valitse Maksuliikenteen hallinta > Takausasiakirjat > Takausasiakirjat.</span><span class="sxs-lookup"><span data-stu-id="46eaa-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="46eaa-198">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="46eaa-199">Avaa valintaikkuna valitsemalla Realisoi.</span><span class="sxs-lookup"><span data-stu-id="46eaa-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="46eaa-200">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="46eaa-200">Click OK.</span></span>
12. <span data-ttu-id="46eaa-201">Laajenna Toiminnot-osa.</span><span class="sxs-lookup"><span data-stu-id="46eaa-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="46eaa-202">Tarkista Realisoi-tietue.</span><span class="sxs-lookup"><span data-stu-id="46eaa-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="46eaa-203">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="46eaa-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="46eaa-204">Avaa Kirjauskansion eränumero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="46eaa-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="46eaa-205">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="46eaa-205">Click Lines.</span></span>
    * <span data-ttu-id="46eaa-206">Tarkista kirjatut kirjauskansioviennit.</span><span class="sxs-lookup"><span data-stu-id="46eaa-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="46eaa-207">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="46eaa-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]