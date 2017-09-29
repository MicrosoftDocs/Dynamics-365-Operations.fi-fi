--- 
title: Myyntitarjousten luonti ja muokkaus
description: "Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f56b495131836689395a2124d5a834579e1646b7
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="32e3e-103">Myyntitarjousten luonti ja muokkaus</span><span class="sxs-lookup"><span data-stu-id="32e3e-103">Create and edit sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32e3e-104">Tässä menettelyssä käsitellään, miten myyntitarjous luodaan ja päivitetään.</span><span class="sxs-lookup"><span data-stu-id="32e3e-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="32e3e-105">Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="32e3e-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="32e3e-106">Luo myyntitarjous</span><span class="sxs-lookup"><span data-stu-id="32e3e-106">Create a sales quotation</span></span>
1. <span data-ttu-id="32e3e-107">Valitse Myynti ja markkinointi > Myyntitarjoukset > Kaikki tarjoukset.</span><span class="sxs-lookup"><span data-stu-id="32e3e-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="32e3e-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="32e3e-108">Click New.</span></span>
3. <span data-ttu-id="32e3e-109">Valitse Tilityyppi-kentässä Prospekti.</span><span class="sxs-lookup"><span data-stu-id="32e3e-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="32e3e-110">Anna tai valitse Prospekti-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="32e3e-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="32e3e-111">Laajenna Yleiset-osa.</span><span class="sxs-lookup"><span data-stu-id="32e3e-111">Expand the General section.</span></span>
    * <span data-ttu-id="32e3e-112">Koska valitsit tarjouksen luomisen Myynti ja markkinointi -alueelta, tyypiksi määritettiin automaattisesti Myyntitarjous.</span><span class="sxs-lookup"><span data-stu-id="32e3e-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="32e3e-113">Jos haluat luoda projektitarjouksen, tee se Projektinhallinta ja kirjanpito -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="32e3e-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="32e3e-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="32e3e-114">Click OK.</span></span>
    * <span data-ttu-id="32e3e-115">Tarjousrivin kentät ja toiminnot muistuttavat myyntitilausrivin kenttiä ja toimintoja.</span><span class="sxs-lookup"><span data-stu-id="32e3e-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="32e3e-116">Myyntitilausten tavoin tarjoukset voidaan luoda tietylle nimikkeelle tai, jos nimiketunnusta ei tiedetä tai sitä ei ole tarjouksen luontiaikana, ne voidaan luoda myyntiluokalle.</span><span class="sxs-lookup"><span data-stu-id="32e3e-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="32e3e-117">Anna tai valitse Nimike-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="32e3e-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="32e3e-118">Kirjoita Nimike-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="32e3e-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="32e3e-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32e3e-119">Close the page.</span></span>
10. <span data-ttu-id="32e3e-120">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32e3e-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="32e3e-121">Jos rivillä valitulla nimikkeellä on voimassaolevia sopimuksia, sovellettava hinta ja alennukset kopioidaan automaattisesti tarjousriville.</span><span class="sxs-lookup"><span data-stu-id="32e3e-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="32e3e-122">Varmista, että Yksikköhinta-kentässä on arvo. Voit halutessasi antaa myös alennusarvot.</span><span class="sxs-lookup"><span data-stu-id="32e3e-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="32e3e-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="32e3e-123">Click Save.</span></span>
12. <span data-ttu-id="32e3e-124">Valitse toimintoruudussa Myyntitarjous.</span><span class="sxs-lookup"><span data-stu-id="32e3e-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="32e3e-125">Valitse Summat.</span><span class="sxs-lookup"><span data-stu-id="32e3e-125">Click Totals.</span></span>
14. <span data-ttu-id="32e3e-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="32e3e-126">Click OK.</span></span>
15. <span data-ttu-id="32e3e-127">Valitse myyntitarjousrivi.</span><span class="sxs-lookup"><span data-stu-id="32e3e-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="32e3e-128">Valitse Hinnat.</span><span class="sxs-lookup"><span data-stu-id="32e3e-128">Click Prices.</span></span>
    * <span data-ttu-id="32e3e-129">Voit kokeilla Suorita hintasimulaatio -sivulla tarjouksen odotetun tuoton tai kannattavuuden säätämistä halutun yksikköhinnan, alennussumman, alennusprosentin, kokonaissumman, marginaalin tai katetuottoprosentin perusteella.</span><span class="sxs-lookup"><span data-stu-id="32e3e-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="32e3e-130">Kun olet tyytyväinen tavoitelukuihin, käytä ehdotusta tarjousrivillä, jolloin sen hintaan liittyvät kentät päivitetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="32e3e-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="32e3e-131">Voit luoda niin monta hintasimulointia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="32e3e-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="32e3e-132">Uusi valitset Uusi, nykyisen tarjousrivin hintaehdot kopioidaan sivulle.</span><span class="sxs-lookup"><span data-stu-id="32e3e-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="32e3e-133">Voit sitten muokata minkä tahansa hintaan liittyvän kentän arvoja tavoitearvoiksi.</span><span class="sxs-lookup"><span data-stu-id="32e3e-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="32e3e-134">Yhden kentän muuttaminen käynnistää kaikkien muiden kenttien uudelleenlaskennan.</span><span class="sxs-lookup"><span data-stu-id="32e3e-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="32e3e-135">Jotta järjestelmä voisi laskea myyntikatteen ja katetuottoprosentin, tuotteen yksikkökustannus on tiedettävä.</span><span class="sxs-lookup"><span data-stu-id="32e3e-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="32e3e-136">Simuloidut hinnat -välilehdessä on tarkat tiedot alkuperäisistä hinnoista, ehdotetuista muutoksista ja niiden vaikutuksesta tarjouksen summiin.</span><span class="sxs-lookup"><span data-stu-id="32e3e-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="32e3e-137">Yleisesti ottaen järjestelmä laskee arvon uudelleen ja lisää uuden arvon Yksikköhinta-kenttään, kun simulointi määrittää, että tarjousrivillä on käytettävä uutta summaa.</span><span class="sxs-lookup"><span data-stu-id="32e3e-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="32e3e-138">Jos simulointi perustuu uuteen marginaaliin tai uuteen katetuottoprosenttiin, vain Nettosumma-kenttä päivitetään ja Yksikköhinta on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="32e3e-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="32e3e-139">Kummassakin tapauksessa tarjousrivillä ennen simulointia olleet alennukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="32e3e-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="32e3e-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32e3e-140">Close the page.</span></span>
18. <span data-ttu-id="32e3e-141">Valitse toimintoruudussa Tarjous.</span><span class="sxs-lookup"><span data-stu-id="32e3e-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="32e3e-142">Valitse Lähetä tarjous.</span><span class="sxs-lookup"><span data-stu-id="32e3e-142">Click Send quotation.</span></span>
20. <span data-ttu-id="32e3e-143">Valitse Tulosta tarjous -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="32e3e-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="32e3e-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="32e3e-144">Click OK.</span></span>
    * <span data-ttu-id="32e3e-145">Raportin luontiin voi kulua useita minuutteja.</span><span class="sxs-lookup"><span data-stu-id="32e3e-145">The report may take a minute to generate.</span></span> <span data-ttu-id="32e3e-146">Älä sulje sivu, ennen kuin raportti on valmis.</span><span class="sxs-lookup"><span data-stu-id="32e3e-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="32e3e-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32e3e-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="32e3e-148">Päivitä myyntitarjous</span><span class="sxs-lookup"><span data-stu-id="32e3e-148">Update a sales quotation</span></span>
1. <span data-ttu-id="32e3e-149">Valitse toimintoruudussa Seuranta.</span><span class="sxs-lookup"><span data-stu-id="32e3e-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="32e3e-150">Valitse Muunna asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="32e3e-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="32e3e-151">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32e3e-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="32e3e-152">Valitse Tarkista.</span><span class="sxs-lookup"><span data-stu-id="32e3e-152">Click Check.</span></span>
    * <span data-ttu-id="32e3e-153">Varmista, että näyttöön avautuu sanoma, jonka mukaan antamasi tilinumero on vapaa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="32e3e-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="32e3e-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="32e3e-154">Click OK.</span></span>
    * <span data-ttu-id="32e3e-155">Järjestelmä on nyt luonut uuden asiakastilin tarjouksen prospektille.</span><span class="sxs-lookup"><span data-stu-id="32e3e-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="32e3e-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32e3e-156">Close the page.</span></span>
7. <span data-ttu-id="32e3e-157">Valitse toimintoruudussa Seuranta.</span><span class="sxs-lookup"><span data-stu-id="32e3e-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="32e3e-158">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="32e3e-158">Click Confirm.</span></span>
9. <span data-ttu-id="32e3e-159">Anna tai valitse Syy-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="32e3e-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="32e3e-160">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="32e3e-160">Click OK.</span></span>
11. <span data-ttu-id="32e3e-161">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="32e3e-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="32e3e-162">Valitse Myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="32e3e-162">Click Sales orders.</span></span>
13. <span data-ttu-id="32e3e-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32e3e-163">Close the page.</span></span>


