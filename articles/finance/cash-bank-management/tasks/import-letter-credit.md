---
title: Tuo remburssi
description: Tässä menettelyssä käsitellään tuontiremburssiprosessi.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76dedb12eef0f8282f04f680cab51a8ccf3e8221
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009540"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="15d93-103">Tuo remburssi</span><span class="sxs-lookup"><span data-stu-id="15d93-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15d93-104">Tässä menettelyssä käsitellään tuontiremburssiprosessi.</span><span class="sxs-lookup"><span data-stu-id="15d93-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="15d93-105">Seuraavat on määritettävä ennen menettelyn suorittamista: pankkilimiitit, kirjausprofiilit, pankin limiittisopimus ja toimittajan pankkitiedot.</span><span class="sxs-lookup"><span data-stu-id="15d93-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="15d93-106">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="15d93-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="15d93-107">Luo myyntitilaus, jossa on remburssi</span><span class="sxs-lookup"><span data-stu-id="15d93-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="15d93-108">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="15d93-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="15d93-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="15d93-109">Click New.</span></span>
3. <span data-ttu-id="15d93-110">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15d93-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="15d93-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="15d93-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="15d93-113">Laajenna Yleinen-osa.</span><span class="sxs-lookup"><span data-stu-id="15d93-113">Expand the General section.</span></span>
7. <span data-ttu-id="15d93-114">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="15d93-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="15d93-116">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="15d93-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="15d93-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="15d93-118">Kirjoita päivämäärä Kirjauspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="15d93-119">Kirjoita päivämäärä Toimituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="15d93-120">Huomautus: Pankkitositteen tyyppi -kenttään on valittava arvo Remburssi.</span><span class="sxs-lookup"><span data-stu-id="15d93-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="15d93-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-121">Click OK.</span></span>
14. <span data-ttu-id="15d93-122">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15d93-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="15d93-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="15d93-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="15d93-125">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="15d93-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="15d93-126">Valitse Toimitus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="15d93-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="15d93-127">Kirjoita päivämäärä Toimituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="15d93-128">Kirjoita päivämäärä Vahvistettu toimituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="15d93-129">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="15d93-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="15d93-130">Määritä remburssin tiedot.</span><span class="sxs-lookup"><span data-stu-id="15d93-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="15d93-131">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="15d93-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="15d93-132">Valitse Remburssi/tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="15d93-133">Anna päivämäärä ja kellonaika Hakemuksen päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="15d93-134">Tarkista, että Pankkitili-kentässä on aktiivinen, käyttöpäivämäärään perustuva oletuspankkitili.</span><span class="sxs-lookup"><span data-stu-id="15d93-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="15d93-135">Kirjoita arvo Pankkitositteen numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="15d93-136">Anna päivämäärä ja kellonaika Vastaanottopäivä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="15d93-137">Laajenna Pankkitosite-osa.</span><span class="sxs-lookup"><span data-stu-id="15d93-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="15d93-138">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="15d93-139">Laajenna Pankin tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="15d93-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="15d93-140">Anna tai valitse Neuvova pankki -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="15d93-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="15d93-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="15d93-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="15d93-142">Click Save.</span></span>
33. <span data-ttu-id="15d93-143">Valitse Hae ostotilauksen lähetykset.</span><span class="sxs-lookup"><span data-stu-id="15d93-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="15d93-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-144">Close the page.</span></span>
35. <span data-ttu-id="15d93-145">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="15d93-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="15d93-146">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="15d93-146">Click Confirm.</span></span>
37. <span data-ttu-id="15d93-147">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="15d93-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="15d93-148">Valitse Remburssi/tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="15d93-149">Valitse Prosessi.</span><span class="sxs-lookup"><span data-stu-id="15d93-149">Click Process.</span></span>
40. <span data-ttu-id="15d93-150">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="15d93-150">Click Confirm.</span></span>
    * <span data-ttu-id="15d93-151">Tarkista, että limiittisaldo pienentää ostotilauksen summaa.</span><span class="sxs-lookup"><span data-stu-id="15d93-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="15d93-152">Tässä esimerkissä ostosumma = 500,00, tositteen limiitti = 10 000,00, joten limiittisaldo = 9 500,00.</span><span class="sxs-lookup"><span data-stu-id="15d93-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="15d93-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-153">Close the page.</span></span>
42. <span data-ttu-id="15d93-154">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="15d93-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="15d93-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="15d93-155">Click Save.</span></span>
44. <span data-ttu-id="15d93-156">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="15d93-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="15d93-157">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="15d93-157">Click Confirm.</span></span>
    * <span data-ttu-id="15d93-158">Muuta remburssia yksikköhinnan muutoksen takia.</span><span class="sxs-lookup"><span data-stu-id="15d93-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="15d93-159">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="15d93-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="15d93-160">Valitse Remburssi/tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="15d93-161">Muuta remburssia ostoyksikön hinnan muutoksen takia.</span><span class="sxs-lookup"><span data-stu-id="15d93-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="15d93-162">Valitse Prosessi.</span><span class="sxs-lookup"><span data-stu-id="15d93-162">Click Process.</span></span>
49. <span data-ttu-id="15d93-163">Valitse Muuta.</span><span class="sxs-lookup"><span data-stu-id="15d93-163">Click Amend.</span></span>
50. <span data-ttu-id="15d93-164">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="15d93-164">Click Remove.</span></span>
51. <span data-ttu-id="15d93-165">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="15d93-165">Click Yes.</span></span>
52. <span data-ttu-id="15d93-166">Valitse Hae ostotilauksen lähetykset.</span><span class="sxs-lookup"><span data-stu-id="15d93-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="15d93-167">Valitse Prosessi.</span><span class="sxs-lookup"><span data-stu-id="15d93-167">Click Process.</span></span>
54. <span data-ttu-id="15d93-168">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="15d93-168">Click Confirm.</span></span>
    * <span data-ttu-id="15d93-169">Tarkista, että limiittisaldo pienentää ostotilauksen summaa.</span><span class="sxs-lookup"><span data-stu-id="15d93-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="15d93-170">Tässä esimerkissä muokattu ostosumma = 600,00, tositteen limiitti = 10 000,00, joten limiittisaldo = 9 400,00.</span><span class="sxs-lookup"><span data-stu-id="15d93-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="15d93-171">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="15d93-172">Kirjaa pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="15d93-172">Post Packing slip</span></span>
1. <span data-ttu-id="15d93-173">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="15d93-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="15d93-174">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="15d93-174">Click Product receipt.</span></span>
3. <span data-ttu-id="15d93-175">Kirjoita PurchParmTable_Num-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="15d93-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="15d93-176">Valitse remburssiviittauksen avulla luotu lähetyksen numero.</span><span class="sxs-lookup"><span data-stu-id="15d93-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="15d93-177">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="15d93-178">Kirjoita päivämäärä Tuotteen vastaanottopäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="15d93-179">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-179">Click OK.</span></span>
7. <span data-ttu-id="15d93-180">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-180">Close the page.</span></span>
8. <span data-ttu-id="15d93-181">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="15d93-182">Tarkista Tuo remburssitapahtuma -tila</span><span class="sxs-lookup"><span data-stu-id="15d93-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="15d93-183">Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="15d93-184">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15d93-185">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15d93-186">Tarkista Tuo remburssitapahtuma -tila.</span><span class="sxs-lookup"><span data-stu-id="15d93-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="15d93-187">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-187">Close the page.</span></span>
5. <span data-ttu-id="15d93-188">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="15d93-189">Kirjaa ostolasku</span><span class="sxs-lookup"><span data-stu-id="15d93-189">Post purchase invoice</span></span>
1. <span data-ttu-id="15d93-190">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="15d93-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="15d93-191">Valitse remburssin avulla luotu ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="15d93-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="15d93-192">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15d93-193">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="15d93-194">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="15d93-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="15d93-195">Valitse lasku.</span><span class="sxs-lookup"><span data-stu-id="15d93-195">Click Invoice.</span></span>
6. <span data-ttu-id="15d93-196">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="15d93-197">Anna tai valitse arvo Lähetyksen numero -kentässä.</span><span class="sxs-lookup"><span data-stu-id="15d93-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="15d93-198">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="15d93-199">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="15d93-200">Valitse Päivitä täsmäytyksen tila.</span><span class="sxs-lookup"><span data-stu-id="15d93-200">Click Update match status.</span></span>
11. <span data-ttu-id="15d93-201">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="15d93-201">Click Post.</span></span>
12. <span data-ttu-id="15d93-202">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-202">Close the page.</span></span>
13. <span data-ttu-id="15d93-203">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="15d93-204">Tarkista Tuo remburssitapahtuma -tila</span><span class="sxs-lookup"><span data-stu-id="15d93-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="15d93-205">Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="15d93-206">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15d93-207">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15d93-208">Tarkista Tuo remburssi2.</span><span class="sxs-lookup"><span data-stu-id="15d93-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="15d93-209">Varmista: Lähetyksen tila = laskutetun pankkilimiitin tiedot</span><span class="sxs-lookup"><span data-stu-id="15d93-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="15d93-210">Valitse Näytä.</span><span class="sxs-lookup"><span data-stu-id="15d93-210">Click View.</span></span>
5. <span data-ttu-id="15d93-211">Valitse Tulosta hakemus.</span><span class="sxs-lookup"><span data-stu-id="15d93-211">Click Print application.</span></span>
6. <span data-ttu-id="15d93-212">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-212">Click OK.</span></span>
    * <span data-ttu-id="15d93-213">Tarkista, että remburssianomus tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="15d93-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="15d93-214">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-214">Close the page.</span></span>
8. <span data-ttu-id="15d93-215">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-215">Close the page.</span></span>
9. <span data-ttu-id="15d93-216">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="15d93-217">Kirjaa luodun remburssin sisältävän ostolaskun toimittajan maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="15d93-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="15d93-218">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="15d93-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="15d93-219">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="15d93-219">Click New.</span></span>
3. <span data-ttu-id="15d93-220">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="15d93-221">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="15d93-222">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="15d93-222">Click Lines.</span></span>
6. <span data-ttu-id="15d93-223">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="15d93-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="15d93-224">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="15d93-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="15d93-225">Valitse Selvitä tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15d93-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="15d93-226">Laajenna Summat-osa.</span><span class="sxs-lookup"><span data-stu-id="15d93-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="15d93-227">Valitse vaihtoehto Näytä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="15d93-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="15d93-228">Tarkista, että Pankkitositteen numero- ja Lähetyksen numero -kentät on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="15d93-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="15d93-229">Valitse Merkitse-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="15d93-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="15d93-230">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-230">Click OK.</span></span>
13. <span data-ttu-id="15d93-231">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="15d93-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="15d93-232">Tarkista, että Pankkitositteen numero- ja Lähetyksen numero -kentät on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="15d93-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="15d93-233">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="15d93-233">Click Post.</span></span>
15. <span data-ttu-id="15d93-234">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-234">Close the page.</span></span>
16. <span data-ttu-id="15d93-235">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="15d93-236">Tarkista Tuo remburssi -tila, kun lasku on maksettu</span><span class="sxs-lookup"><span data-stu-id="15d93-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="15d93-237">Valitse Maksuliikenteen hallinta > Luottokirjeet > Tuontiremburssi ja tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="15d93-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="15d93-238">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15d93-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="15d93-239">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="15d93-240">Tarkista Tuo remburssitapahtuma -tila.</span><span class="sxs-lookup"><span data-stu-id="15d93-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="15d93-241">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="15d93-242">Tarkista pankkilimiitti ja käyttöraportti</span><span class="sxs-lookup"><span data-stu-id="15d93-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="15d93-243">Valitse Maksuliikenteen hallinta > Kyselyt ja raportit > Luottokirjeet tai takaukset > Pankkipalvelut ja käyttö -raportti.</span><span class="sxs-lookup"><span data-stu-id="15d93-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="15d93-244">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="15d93-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="15d93-245">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="15d93-245">Click Filter.</span></span>
    * <span data-ttu-id="15d93-246">Määritä Ehdot-kenttä pakollisen pankkitilin avulla.</span><span class="sxs-lookup"><span data-stu-id="15d93-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="15d93-247">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="15d93-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="15d93-248">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15d93-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="15d93-249">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-249">Click OK.</span></span>
7. <span data-ttu-id="15d93-250">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15d93-250">Click OK.</span></span>
    * <span data-ttu-id="15d93-251">Tarkista tapahtumat sisältävä raportti.</span><span class="sxs-lookup"><span data-stu-id="15d93-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="15d93-252">Tarkista, että raportin tapahtumissa on mainittu pankkitositteen numero, tositteen limiitti, käytetty summa ja limiittisaldo.</span><span class="sxs-lookup"><span data-stu-id="15d93-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="15d93-253">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="15d93-253">Close the page.</span></span>

