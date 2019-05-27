---
title: Vientiremburssit
description: Tässä menettelyssä käsitellään vientiremburssiprosessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566153"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="cddc6-103">Vientiremburssit</span><span class="sxs-lookup"><span data-stu-id="cddc6-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cddc6-104">Tässä menettelyssä käsitellään vientiremburssiprosessi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="cddc6-105">Remburssi on pankin antama sopimus, jossa pankki suostuu varmistamaan maksun ostajan puolesta, jos ostajan ja myyjän väliset ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="cddc6-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="cddc6-106">Suorittaa Määritä pankin limiitit ja kirjausprofiilit - ja Luo pankin limiittisopimus remburssia varten -menettelyt ennen tätä menettelyä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="cddc6-107">USMF-demoyritys on oltava valittuna, muuten menettelyn suorittaminen ei onnistu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="cddc6-108">Luo myyntitilaus vientiremburssille</span><span class="sxs-lookup"><span data-stu-id="cddc6-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="cddc6-109">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="cddc6-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="cddc6-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-110">Click New.</span></span>
3. <span data-ttu-id="cddc6-111">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cddc6-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cddc6-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cddc6-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cddc6-114">Laajenna tai tiivistä Yleiset-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="cddc6-115">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="cddc6-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cddc6-116">Valitse toimipaikka, johon otettava nimike on varastoitu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="cddc6-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cddc6-118">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cddc6-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cddc6-119">Valitse varasto, johon otettava nimike on varastoitu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="cddc6-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cddc6-121">Huomautus: Pankkitositteen tyyppi -kenttään on valittava arvo Remburssi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="cddc6-122">Valitse Pankkitositteen tyyppi -kentässä Remburssi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="cddc6-123">Laajenna tai tiivistä Toimitus-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="cddc6-124">Valitse Toimituspäivän tarkistus = Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="cddc6-125">Kirjoita päivämäärä Pyydetty vastaanottopäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="cddc6-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-126">Click OK.</span></span>
15. <span data-ttu-id="cddc6-127">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cddc6-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cddc6-128">Valitse otettava tai myytävä pakollinen nimike.</span><span class="sxs-lookup"><span data-stu-id="cddc6-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="cddc6-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="cddc6-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cddc6-131">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cddc6-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="cddc6-132">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="cddc6-133">Valitse Toimitus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="cddc6-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="cddc6-134">Kirjoita päivämäärä Pyydetty lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="cddc6-135">Kirjoita päivämäärä Vahvistettu lähetyspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="cddc6-136">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="cddc6-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="cddc6-137">Valitse Remburssi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="cddc6-138">Kirjoita arvo Pankkitositteen numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="cddc6-139">Anna päivämäärä ja kellonaika Vanhentumispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="cddc6-140">Laajenna tai tiivistä Pankin tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="cddc6-141">Avaa haku napsauttamalla Liikkeelle laskeva pankki -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="cddc6-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="cddc6-142">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="cddc6-143">Avaa haku napsauttamalla Neuvova pankki -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="cddc6-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="cddc6-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="cddc6-145">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="cddc6-146">Valitse Hae myyntitilauksen lähetykset.</span><span class="sxs-lookup"><span data-stu-id="cddc6-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="cddc6-147">Valitse Liikkeeseen laskevan pankin asiakirja.</span><span class="sxs-lookup"><span data-stu-id="cddc6-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="cddc6-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="cddc6-149">Kirjaa pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="cddc6-149">Post Packing slip</span></span>
1. <span data-ttu-id="cddc6-150">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="cddc6-151">Valitse Kirjaa pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="cddc6-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="cddc6-152">Laajenna tai tiivistä Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="cddc6-153">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="cddc6-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="cddc6-154">Laajenna tai tiivistä Asetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="cddc6-155">Kirjoita päivämäärä Pakkausluettelon päiväys -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="cddc6-156">Valitse Lähetyksen numero.</span><span class="sxs-lookup"><span data-stu-id="cddc6-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="cddc6-157">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cddc6-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-158">Click OK.</span></span>
10. <span data-ttu-id="cddc6-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="cddc6-160">Kirjaa myyntilasku</span><span class="sxs-lookup"><span data-stu-id="cddc6-160">Post sales invoice</span></span>
1. <span data-ttu-id="cddc6-161">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="cddc6-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="cddc6-162">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="cddc6-162">Click Invoice.</span></span>
3. <span data-ttu-id="cddc6-163">Laajenna tai tiivistä Yhteenveto-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="cddc6-164">Valitse Lähetyksen numero.</span><span class="sxs-lookup"><span data-stu-id="cddc6-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="cddc6-165">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cddc6-166">Laajenna tai tiivistä Asetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="cddc6-167">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="cddc6-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="cddc6-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-168">Click OK.</span></span>
9. <span data-ttu-id="cddc6-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="cddc6-170">Lähetysasiakirjojen lähetystila</span><span class="sxs-lookup"><span data-stu-id="cddc6-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="cddc6-171">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="cddc6-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="cddc6-172">Valitse Remburssi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="cddc6-173">Laajenna tai tiivistä Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="cddc6-174">Huomautus: Asiakirja lähetetty -kentässä on oltava valittuna Kyllä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="cddc6-175">Tarkista vientiremburssi</span><span class="sxs-lookup"><span data-stu-id="cddc6-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="cddc6-176">Valitse Maksuliikenteen hallinta > Luottokirjeet > Vientiremburssi ja tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="cddc6-177">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cddc6-178">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cddc6-179">Tarkista, vientiremburssin lähetyksen tila on Laskutettu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="cddc6-180">Asiakkaan maksu</span><span class="sxs-lookup"><span data-stu-id="cddc6-180">Customer payment</span></span>
1. <span data-ttu-id="cddc6-181">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="cddc6-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="cddc6-182">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-182">Click New.</span></span>
3. <span data-ttu-id="cddc6-183">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cddc6-184">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="cddc6-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cddc6-185">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cddc6-186">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="cddc6-186">Click Lines.</span></span>
7. <span data-ttu-id="cddc6-187">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="cddc6-188">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="cddc6-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="cddc6-189">Valitse Tilitys.</span><span class="sxs-lookup"><span data-stu-id="cddc6-189">Click Settlement.</span></span>
10. <span data-ttu-id="cddc6-190">Valitse Summat-otsikon valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="cddc6-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="cddc6-191">Huomautus: valitse Näytä-kentän asetukseksi Remburssi.</span><span class="sxs-lookup"><span data-stu-id="cddc6-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="cddc6-192">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="cddc6-193">Valitse Merkitse-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="cddc6-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="cddc6-194">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cddc6-194">Click OK.</span></span>
14. <span data-ttu-id="cddc6-195">Valitse Maksu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="cddc6-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="cddc6-196">Tarkista Pankkitositteen numero- ja Lähetyksen numero -asetusten tiedot</span><span class="sxs-lookup"><span data-stu-id="cddc6-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="cddc6-197">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="cddc6-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="cddc6-198">Tarkista vientiremburssi maksun jälkeen</span><span class="sxs-lookup"><span data-stu-id="cddc6-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="cddc6-199">Valitse Maksuliikenteen hallinta > Luottokirjeet > Vientiremburssi ja tuontiperintä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="cddc6-200">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="cddc6-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cddc6-201">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="cddc6-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cddc6-202">Tarkista, että Lähetyksen tila = Maksu vastaanotettu ja saldon summa = 0,00.</span><span class="sxs-lookup"><span data-stu-id="cddc6-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

