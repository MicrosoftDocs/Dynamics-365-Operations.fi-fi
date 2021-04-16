---
title: Ostoreskontran avaintiedot toimittajan laskua käyttämällä
description: Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d3f9fc1fb7724632dbc9c4c3e1e28c6e85eaf61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827791"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="0fef0-103">Ostoreskontran avaintiedot toimittajan laskua käyttämällä</span><span class="sxs-lookup"><span data-stu-id="0fef0-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fef0-104">Tämän tehtäväoppaan avulla voit luoda toimittajan laskun ostotilauksesta ja tarkastella ostotilauksen, vastaanoton ja laskun (kolmisuuntainen täsmäytys) täsmäytyksen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="0fef0-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0fef0-105">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="0fef0-105">Create a purchase order</span></span>
1. <span data-ttu-id="0fef0-106">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="0fef0-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-107">Click **New**.</span></span>
3. <span data-ttu-id="0fef0-108">Avaa haku valitsemalla **Toimittajan tili** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0fef0-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0fef0-109">Etsi toimittaja ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0fef0-109">Find a vendor to select.</span></span> <span data-ttu-id="0fef0-110">Voit esimerkiksi siirtyä kohtaan US-104.</span><span class="sxs-lookup"><span data-stu-id="0fef0-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="0fef0-111">Valitse toimittaja US-104.</span><span class="sxs-lookup"><span data-stu-id="0fef0-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="0fef0-112">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-112">Click **OK**.</span></span>
7. <span data-ttu-id="0fef0-113">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0fef0-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0fef0-114">Valitse varastonimike.</span><span class="sxs-lookup"><span data-stu-id="0fef0-114">Select an inventory item.</span></span> <span data-ttu-id="0fef0-115">Valitse tässä esimerkissä nimiketunnus 1000.</span><span class="sxs-lookup"><span data-stu-id="0fef0-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="0fef0-116">Laajenna **Rivin erittely** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="0fef0-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="0fef0-117">Valitse **Asetukset**-välilehti. Voit korvata täsmäytyskäytännön niin, että täsmäytystä ei käytetä tai että käytössä on kaksi- tai kolmisuuntainen täsmäytys.</span><span class="sxs-lookup"><span data-stu-id="0fef0-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="0fef0-118">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="0fef0-119">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="0fef0-120">Vastaanota tuotteet</span><span class="sxs-lookup"><span data-stu-id="0fef0-120">Receive the products</span></span>
1. <span data-ttu-id="0fef0-121">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="0fef0-122">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="0fef0-123">Syötä **Tuotteen vastaanotto** -kenttään tuotteen vastaanottonumero.</span><span class="sxs-lookup"><span data-stu-id="0fef0-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="0fef0-124">Syötä arvoksi esimerkiksi PR123.</span><span class="sxs-lookup"><span data-stu-id="0fef0-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="0fef0-125">Kirjaa tuotteen vastaanotto valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="0fef0-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fef0-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="0fef0-127">Luo toimittajan lasku</span><span class="sxs-lookup"><span data-stu-id="0fef0-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="0fef0-128">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Vastaanotetut ostotilaukset, joita ei ole laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="0fef0-129">Valitse luomasi ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="0fef0-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="0fef0-130">Valitse toimintoruudussa **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="0fef0-131">Valitse **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="0fef0-132">Syötä **Numero**-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="0fef0-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="0fef0-133">Kirjoita arvo **Laskun kuvaus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0fef0-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="0fef0-134">Syötä **Laskun päivämäärä** -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="0fef0-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="0fef0-135">Syötä **Yksikköhinta**-kentän arvoksi 1 200.</span><span class="sxs-lookup"><span data-stu-id="0fef0-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="0fef0-136">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-136">Click **Add line**.</span></span>
10. <span data-ttu-id="0fef0-137">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0fef0-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0fef0-138">Etsi asennuskulun nimiketunnus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0fef0-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="0fef0-139">Syötä arvoksi esimerkiksi S0001</span><span class="sxs-lookup"><span data-stu-id="0fef0-139">For example, S0001</span></span>
12. <span data-ttu-id="0fef0-140">Valitse asennuskulun nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="0fef0-140">Select the installation charge item number.</span></span> <span data-ttu-id="0fef0-141">Huomaa, että täsmäytystä ei ole suoritettu, koska teit muutoksia.</span><span class="sxs-lookup"><span data-stu-id="0fef0-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="0fef0-142">Valitse **Päivitä täsmäytyksen tila**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="0fef0-143">Valitse toimintoruudussa **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="0fef0-144">Valitse **Täsmäytyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-144">Click **Matching details**.</span></span> <span data-ttu-id="0fef0-145">Uuden palveluita sisältävää riviä ei tarvitse täsmäyttää, joten tilana pysyy Ei suoritettu.</span><span class="sxs-lookup"><span data-stu-id="0fef0-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="0fef0-146">Valitse tuotteen vastaanotto vastaanottamasi varastonimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="0fef0-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="0fef0-147">Tuotteen vastaanoton sisältävä rivi täsmäytettiin, mutta se sisälsi määrän tai hinnan ristiriidan, joten täsmäytys epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="0fef0-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="0fef0-148">Syötä **Yksikköhinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0fef0-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="0fef0-149">Nyt, kun yksikköhinta täsmää, tilaksi päivitetään Hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="0fef0-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="0fef0-150">Jos käytäntö sallii ristiriidat tai jos täsmäytys on vain varoitus, voit kirjata laskun.</span><span class="sxs-lookup"><span data-stu-id="0fef0-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="0fef0-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fef0-151">Close the page.</span></span>
19. <span data-ttu-id="0fef0-152">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="0fef0-152">Click **Post**.</span></span>
20. <span data-ttu-id="0fef0-153">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="0fef0-153">Close the form.</span></span> <span data-ttu-id="0fef0-154">Huomaa, että ostotilaus on vastaanotettujen luettelon sijaan laskuttamattomien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0fef0-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]