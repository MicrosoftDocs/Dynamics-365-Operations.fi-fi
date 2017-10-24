--- 
title: Asiakkaan maksun yhteenveto
description: "Tässä tehtävän ohjauksessa kerrotaan asiakkaan maksujen syöttämisessä käytettävät tavat."
author: kweekley
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e6e10d0d0a05b0594ba5cf6a77f474b461bd9dca
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="customer-payment-overview"></a><span data-ttu-id="40bd7-103">Asiakkaan maksun yhteenveto</span><span class="sxs-lookup"><span data-stu-id="40bd7-103">Customer payment overview</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40bd7-104">Tässä tehtävän ohjauksessa kerrotaan asiakkaan maksujen syöttämisessä käytettävät tavat.</span><span class="sxs-lookup"><span data-stu-id="40bd7-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="40bd7-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="40bd7-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="40bd7-106">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="40bd7-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="40bd7-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="40bd7-107">Click New.</span></span>
3. <span data-ttu-id="40bd7-108">Valitse maksukirjauskansio, johon asiakkaan maksut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="40bd7-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="40bd7-109">Valitse kirjauskansio tai syötä se manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="40bd7-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="40bd7-110">Valitse Lisää asiakkaan maksuja.</span><span class="sxs-lookup"><span data-stu-id="40bd7-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="40bd7-111">Lisää asiakkaan maksuja -sivua käytetään tallennettaessa yksi asiakkaan maksu kerralla.</span><span class="sxs-lookup"><span data-stu-id="40bd7-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="40bd7-112">Voit syöttää samalla sivulla maksun tiedot (sivun yläosassa) ja maksun yhteydessä maksetut laskut.</span><span class="sxs-lookup"><span data-stu-id="40bd7-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="40bd7-113">Syötä asiakas, jolta vastaanotit maksun.</span><span class="sxs-lookup"><span data-stu-id="40bd7-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="40bd7-114">Jos et tiedä asiakasta, mutta tiedät maksetun tapahtuman, voit syöttää maksun Tapahtuma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="40bd7-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="40bd7-115">Syötä tai valitse lasku Tapahtuma-kentässä.</span><span class="sxs-lookup"><span data-stu-id="40bd7-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="40bd7-116">Asiakas haetaan automaattisesti tapahtuman valitsemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="40bd7-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="40bd7-117">Syötä Maksuviite-kenttään maksuviite.</span><span class="sxs-lookup"><span data-stu-id="40bd7-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="40bd7-118">Maksuviite voi olla asiakkaan sekkinumero tai asiakkaan sähköisen maksun viite.</span><span class="sxs-lookup"><span data-stu-id="40bd7-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="40bd7-119">Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="40bd7-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="40bd7-120">Määritä, sisällytetäänkö maksu tallennuskuittiin.</span><span class="sxs-lookup"><span data-stu-id="40bd7-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="40bd7-121">Syötä asiakkaan maksun summa.</span><span class="sxs-lookup"><span data-stu-id="40bd7-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="40bd7-122">Maksun summaa ei haeta automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="40bd7-122">The payment amount will not default.</span></span> <span data-ttu-id="40bd7-123">Se on syötettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="40bd7-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="40bd7-124">Merkitse asiakkaan maksamat laskut.</span><span class="sxs-lookup"><span data-stu-id="40bd7-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="40bd7-125">Jos maksu ennakkomaksu, laskuja ei tarvitse merkitä selvitystä varten.</span><span class="sxs-lookup"><span data-stu-id="40bd7-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="40bd7-126">Maksun voi silti tallentaa ja kirjata.</span><span class="sxs-lookup"><span data-stu-id="40bd7-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="40bd7-127">Laskun selvitys voidaan tehdä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="40bd7-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="40bd7-128">Syötä sen maksun summa, joka selvitetään merkitylle laskulle.</span><span class="sxs-lookup"><span data-stu-id="40bd7-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="40bd7-129">Tätä kenttää voi käyttää, kun maksu koskee osittaista maksua.</span><span class="sxs-lookup"><span data-stu-id="40bd7-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="40bd7-130">Jos et syötä summaa, selvitettävä summa määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="40bd7-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="40bd7-131">Valitse Tallenna kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="40bd7-131">Click Save in journal.</span></span>
    * <span data-ttu-id="40bd7-132">Ennen kuin tallennat maksun kirjauskansioon, varmista, että vastatili on määritetty.</span><span class="sxs-lookup"><span data-stu-id="40bd7-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="40bd7-133">Kun kirjauskansiossa käytetään Tallenna-toimintoa, maksu tallennetaan ja siirretään kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="40bd7-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="40bd7-134">Tämän jälkeen voit jatkaa seuraavan maksun syöttämistä.</span><span class="sxs-lookup"><span data-stu-id="40bd7-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="40bd7-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="40bd7-135">Close the page.</span></span>
14. <span data-ttu-id="40bd7-136">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="40bd7-136">Click Lines.</span></span>
    * <span data-ttu-id="40bd7-137">Kun avaat Rivit-kohdan, näkyviin tulevat Lisää asiakkaan maksuja -sivulla tallennetut ja kirjauskansioon siirretyt maksut.</span><span class="sxs-lookup"><span data-stu-id="40bd7-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="40bd7-138">Tällä sivuilla voi myös syöttää uusia asiakkaan maksuja tai muokata aiemmin luotuja asiakkaan maksuja, ennen kuin ne kirjataan.</span><span class="sxs-lookup"><span data-stu-id="40bd7-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="40bd7-139">Luo toinen maksu valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="40bd7-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="40bd7-140">Valitse asiakas, jolta vastaanotit maksun.</span><span class="sxs-lookup"><span data-stu-id="40bd7-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="40bd7-141">Jos et tiedä asiakasta, mutta tiedät, että maksun lasku on maksettu, syötä lasku manuaalisesti Lasku-kenttään tai valitse lasku siellä.</span><span class="sxs-lookup"><span data-stu-id="40bd7-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="40bd7-142">Asiakas määritetään, kun lasku on valittu.</span><span class="sxs-lookup"><span data-stu-id="40bd7-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="40bd7-143">Merkitse maksetut laskut valitsemalla Selvitä tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="40bd7-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="40bd7-144">Yhdenkään laskun maksua ei tarvitse selvittää.</span><span class="sxs-lookup"><span data-stu-id="40bd7-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="40bd7-145">Jos tämä on ennakkomaksu tai jos et tiedä maksettua laskua, voit syöttää ja kirjata maksun.</span><span class="sxs-lookup"><span data-stu-id="40bd7-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="40bd7-146">Maksu voidaan tilittää laskulle myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="40bd7-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="40bd7-147">Merkitse maksussa maksetut laskut.</span><span class="sxs-lookup"><span data-stu-id="40bd7-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="40bd7-148">Syötä sen maksun summa, joka selvitetään laskulle.</span><span class="sxs-lookup"><span data-stu-id="40bd7-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="40bd7-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="40bd7-149">Click OK.</span></span>
21. <span data-ttu-id="40bd7-150">Syötä Maksuviite-kenttään maksuviite.</span><span class="sxs-lookup"><span data-stu-id="40bd7-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="40bd7-151">.</span><span class="sxs-lookup"><span data-stu-id="40bd7-151">.</span></span>
    * <span data-ttu-id="40bd7-152">Maksuviite vaaditaan vain, jos maksu on merkitty talletuskuittiin sisällytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="40bd7-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="40bd7-153">Kirjaa asiakkaan maksut.</span><span class="sxs-lookup"><span data-stu-id="40bd7-153">Post the customer payments.</span></span> 


