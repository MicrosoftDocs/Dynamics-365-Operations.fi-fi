--- 
title: "Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla"
description: "Tässä tehtävän ohjauksessa kerrotaan, miten laskurekisteriä käytetään laskujen luomiseen."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="15282-103">Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla</span><span class="sxs-lookup"><span data-stu-id="15282-103">Key invoice data into the AP system using invoice pool</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15282-104">Tässä tehtävän ohjauksessa kerrotaan, miten laskurekisteriä käytetään laskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="15282-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="15282-105">Käytä sitten laskupoolia laskun ja ostotilauksen täsmäyttämisessä ja viimeistele kulu toimittajan laskun sivulla.</span><span class="sxs-lookup"><span data-stu-id="15282-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="15282-106">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="15282-106">Create a purchase order</span></span>
1. <span data-ttu-id="15282-107">Valitse Ostoreskontra > Ostotilaukset > Ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="15282-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="15282-108">Luo ostotilaus valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="15282-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="15282-109">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="15282-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="15282-110">Valitse toimittaja luettelosta.</span><span class="sxs-lookup"><span data-stu-id="15282-110">Select the vendor from the list.</span></span> <span data-ttu-id="15282-111">Voit valita esimerkiksi toimittajan 1001.</span><span class="sxs-lookup"><span data-stu-id="15282-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="15282-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="15282-112">Click OK.</span></span>
6. <span data-ttu-id="15282-113">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="15282-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="15282-114">Etsi luettelosta palveluiden nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="15282-114">Find the services item number in the list.</span></span> <span data-ttu-id="15282-115">Voit valita esimerkiksi arvon S0001.</span><span class="sxs-lookup"><span data-stu-id="15282-115">For example, select S0001.</span></span>
8. <span data-ttu-id="15282-116">Napsauta nimiketunnusta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="15282-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="15282-117">Nettosumma on 75,00 euroa.</span><span class="sxs-lookup"><span data-stu-id="15282-117">The net amount is 75.00.</span></span>  <span data-ttu-id="15282-118">Tämä on laskuun odotettava summa.</span><span class="sxs-lookup"><span data-stu-id="15282-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="15282-119">Valitse toimintoruudussa Osto.</span><span class="sxs-lookup"><span data-stu-id="15282-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="15282-120">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="15282-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="15282-121">Luominen, kirjaaminen ja laskuttaminen</span><span class="sxs-lookup"><span data-stu-id="15282-121">Create and post and invoice</span></span>
1. <span data-ttu-id="15282-122">Siirry kohtaan Ostoreskontra > Laskut > Laskurekisteri.</span><span class="sxs-lookup"><span data-stu-id="15282-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="15282-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="15282-123">Click New.</span></span>
3. <span data-ttu-id="15282-124">Avaa haku, kun haluat valita käytettävän laskurekisterin nimen.</span><span class="sxs-lookup"><span data-stu-id="15282-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="15282-125">Valitse sen laskurekisterin nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="15282-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="15282-126">Valitse Rivit, kun haluat avata rekisterin ja syöttää kulurivejä.</span><span class="sxs-lookup"><span data-stu-id="15282-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="15282-127">Valitse toimittaja haun avulla.</span><span class="sxs-lookup"><span data-stu-id="15282-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="15282-128">Valitse esimerkiksi toimittaja 1001.</span><span class="sxs-lookup"><span data-stu-id="15282-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="15282-129">Syötä Lasku-kenttään laskunumero.</span><span class="sxs-lookup"><span data-stu-id="15282-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="15282-130">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="15282-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="15282-131">Syötä Kredit-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="15282-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="15282-132">Avaa haku valitsemalla Ostotilaus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="15282-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="15282-133">Valitse aiemmin luomasi ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="15282-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="15282-134">Avaa haku valitsemalla Hyväksynyt-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="15282-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="15282-135">Korosta hyväksyjä ja valitse hyväksyjä valitsemalla Valitse.</span><span class="sxs-lookup"><span data-stu-id="15282-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="15282-136">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="15282-136">Click Post.</span></span>
15. <span data-ttu-id="15282-137">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="15282-137">Close the form.</span></span>
16. <span data-ttu-id="15282-138">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="15282-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="15282-139">Laskutusprosessin tekeminen valmiiksi avaamalla lasku poolista ja täsmäyttämällä se ostotilauksen kanssa</span><span class="sxs-lookup"><span data-stu-id="15282-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="15282-140">Siirry kohtaan Ostoreskontra > Laskut > Laskupooli.</span><span class="sxs-lookup"><span data-stu-id="15282-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="15282-141">Luo toimittajan lasku poolissa olevasta laskusta valitsemalla Ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="15282-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="15282-142">Valitse lasku, jota haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="15282-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="15282-143">Tee täsmäytys valmiiksi valitsemalla Päivitä täsmäytyksen tila.</span><span class="sxs-lookup"><span data-stu-id="15282-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="15282-144">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="15282-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="15282-145">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="15282-145">Click Change view.</span></span>
7. <span data-ttu-id="15282-146">Valitse Ruudukkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="15282-146">Click Grid view.</span></span>
8. <span data-ttu-id="15282-147">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="15282-147">Click Post.</span></span>
9. <span data-ttu-id="15282-148">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="15282-148">Close the form.</span></span>
10. <span data-ttu-id="15282-149">Valitse Ostoreskontra > Toimittajat > Toimittajat.</span><span class="sxs-lookup"><span data-stu-id="15282-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="15282-150">Valitse ostotilauksessa mainittu toimittaja.</span><span class="sxs-lookup"><span data-stu-id="15282-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="15282-151">Voit valita esimerkiksi toimittajan 1001.</span><span class="sxs-lookup"><span data-stu-id="15282-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="15282-152">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="15282-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="15282-153">Valitse toimintoruudussa Toimittaja.</span><span class="sxs-lookup"><span data-stu-id="15282-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="15282-154">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15282-154">Click Transactions.</span></span>
15. <span data-ttu-id="15282-155">Valitse luomasi lasku.</span><span class="sxs-lookup"><span data-stu-id="15282-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="15282-156">Laskurekisterin jaksotus peruutettiin ja kirjattiin sopivalle kulutilille.</span><span class="sxs-lookup"><span data-stu-id="15282-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


