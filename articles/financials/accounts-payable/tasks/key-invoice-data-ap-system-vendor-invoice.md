---
title: Ostoreskontrajärjestelmän avaintiedot toimittajan laskua käyttämällä
description: Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "359103"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="ad8bb-103">Ostoreskontrajärjestelmän avaintiedot toimittajan laskua käyttämällä</span><span class="sxs-lookup"><span data-stu-id="ad8bb-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad8bb-104">Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="ad8bb-105">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="ad8bb-105">Create a purchase order</span></span>
1. <span data-ttu-id="ad8bb-106">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ad8bb-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-107">Click New.</span></span>
3. <span data-ttu-id="ad8bb-108">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ad8bb-109">Etsi toimittaja ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-109">Find a vendor to select.</span></span> <span data-ttu-id="ad8bb-110">Voit esimerkiksi siirtyä kohtaan US-104.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="ad8bb-111">Valitse toimittaja US-104.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="ad8bb-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-112">Click OK.</span></span>
7. <span data-ttu-id="ad8bb-113">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ad8bb-114">Valitse varastonimike.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-114">Select an inventory item.</span></span> <span data-ttu-id="ad8bb-115">Valitse tässä esimerkissä nimiketunnus 1000.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="ad8bb-116">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="ad8bb-117">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="ad8bb-118">Voit korvata täsmäytyskäytännön niin, että täsmäytystä ei käytetä tai että käytössä on kaksi- tai kolmisuuntainen täsmäytys.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="ad8bb-119">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="ad8bb-120">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="ad8bb-121">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="ad8bb-122">Vastaanota tuotteet</span><span class="sxs-lookup"><span data-stu-id="ad8bb-122">Receive the products</span></span>
1. <span data-ttu-id="ad8bb-123">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="ad8bb-124">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-124">Click Product receipt.</span></span>
3. <span data-ttu-id="ad8bb-125">Syötä Tuotteen vastaanotto -kenttään tuotteen vastaanottonumero.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="ad8bb-126">Syötä arvoksi esimerkiksi PR123.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="ad8bb-127">Kirjaa tuotteen vastaanotto valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="ad8bb-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="ad8bb-129">Luo toimittajan lasku</span><span class="sxs-lookup"><span data-stu-id="ad8bb-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="ad8bb-130">Siirry kohtaan Ostoreskontra > Ostotilaukset > Vastaanotetut ostotilaukset, joita ei ole laskutettu.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="ad8bb-131">Valitse luomasi ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="ad8bb-132">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="ad8bb-133">Valitse lasku.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-133">Click Invoice.</span></span>
5. <span data-ttu-id="ad8bb-134">Syötä Numero-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="ad8bb-135">Kirjoita arvo Laskun kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="ad8bb-136">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="ad8bb-137">Syötä Yksikköhinta-kentän arvoksi 1200.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="ad8bb-138">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-138">Click Add line.</span></span>
10. <span data-ttu-id="ad8bb-139">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ad8bb-140">Etsi asennuskulun nimiketunnus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="ad8bb-141">Syötä arvoksi esimerkiksi S0001</span><span class="sxs-lookup"><span data-stu-id="ad8bb-141">For example, S0001</span></span>
12. <span data-ttu-id="ad8bb-142">Valitse asennuskulun nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="ad8bb-143">Huomaa, että täsmäytystä ei ole suoritettu, koska teit muutoksia.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="ad8bb-144">Valitse Päivitä täsmäytyksen tila.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-144">Click Update match status.</span></span>
14. <span data-ttu-id="ad8bb-145">Valitse toimintoruudussa Tarkista.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="ad8bb-146">Valitse Täsmäytyksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-146">Click Matching details.</span></span>
    * <span data-ttu-id="ad8bb-147">Uuden palveluita sisältävää riviä ei tarvitse täsmäyttää, joten tilana pysyy Ei suoritettu.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="ad8bb-148">Valitse tuotteen vastaanotto vastaanottamasi varastonimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="ad8bb-149">Tuotteen vastaanoton sisältävä rivi täsmäytettiin, mutta se sisälsi määrän tai hinnan ristiriidan, joten täsmäytys epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="ad8bb-150">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="ad8bb-151">Nyt, kun yksikköhinta täsmää, tilaksi päivitetään Hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="ad8bb-152">Jos käytäntö sallii ristiriidat tai jos täsmäytys on vain varoitus, voit kirjata laskun.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="ad8bb-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-153">Close the page.</span></span>
19. <span data-ttu-id="ad8bb-154">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-154">Click Post.</span></span>
20. <span data-ttu-id="ad8bb-155">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-155">Close the form.</span></span>
    * <span data-ttu-id="ad8bb-156">Huomaa, että ostotilaus on vastaanotettujen luettelon sijaan laskuttamattomien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ad8bb-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

