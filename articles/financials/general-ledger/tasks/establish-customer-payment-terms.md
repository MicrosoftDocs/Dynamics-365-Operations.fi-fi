--- 
title: Muodosta asiakkaan maksuehdot
description: "Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c35c608dc5e9b4790a81a8dadb716157fa740e8c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="9d765-103">Muodosta asiakkaan maksuehdot</span><span class="sxs-lookup"><span data-stu-id="9d765-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d765-104">Tämä menettely määrittää käteisalennuksen ja eräpäivän asetukset.</span><span class="sxs-lookup"><span data-stu-id="9d765-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="9d765-105">Tässä tehtävän ohjauksessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="9d765-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="9d765-106">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksupäivät.</span><span class="sxs-lookup"><span data-stu-id="9d765-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="9d765-107">Myynti- ja ostoreskontran maksuehdot ovat samat.</span><span class="sxs-lookup"><span data-stu-id="9d765-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="9d765-108">Jos määrität ne moduulissa, ne ovat käytettävissä myös toisessa moduulissa.</span><span class="sxs-lookup"><span data-stu-id="9d765-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="9d765-109">Tätä tehtävän ohjausta varten määritetään maksuehdot myyntireskontran puolella.</span><span class="sxs-lookup"><span data-stu-id="9d765-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="9d765-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d765-110">Click New.</span></span>
    * <span data-ttu-id="9d765-111">Luo maksupäivä, jos maksuehdot vaativat tietyn viikonpäivän (maanantai, tiistai jne.) tai tietyn kuukaudenpäivän (5., 10. jne.).</span><span class="sxs-lookup"><span data-stu-id="9d765-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="9d765-112">Syötä Maksupäivä-kenttään maksupäiväkentän tunnus.</span><span class="sxs-lookup"><span data-stu-id="9d765-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="9d765-113">Syötä Kuvaus-kenttään maksupäivän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="9d765-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="9d765-114">Valitse Viikko/Kuukausi-kentässä Viikko tai Kuukausi.</span><span class="sxs-lookup"><span data-stu-id="9d765-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="9d765-115">Jos haluat syöttää viikonpäivän, kuten maanantain, valitse Viikko.</span><span class="sxs-lookup"><span data-stu-id="9d765-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="9d765-116">Jos haluat syöttää kuukaudenpäivän, kuten 10. päivä, valitse Kuukausi.</span><span class="sxs-lookup"><span data-stu-id="9d765-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="9d765-117">Tässä esimerkissä valitaan Kuukausi.</span><span class="sxs-lookup"><span data-stu-id="9d765-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="9d765-118">Syötä Kuukaudenpäivä-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="9d765-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="9d765-119">Päivämäärä syötetään numeroina, eli esim. 10. päivä.</span><span class="sxs-lookup"><span data-stu-id="9d765-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="9d765-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d765-120">Click Save.</span></span>
8. <span data-ttu-id="9d765-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d765-121">Close the page.</span></span>
9. <span data-ttu-id="9d765-122">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksuehdot.</span><span class="sxs-lookup"><span data-stu-id="9d765-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="9d765-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d765-123">Click New.</span></span>
    * <span data-ttu-id="9d765-124">Maksuehtoja käytetään eräpäivien laskennassa.</span><span class="sxs-lookup"><span data-stu-id="9d765-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="9d765-125">Käteisalennuksen päivämäärän asetukset määritetään erillisellä sivulla.</span><span class="sxs-lookup"><span data-stu-id="9d765-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="9d765-126">Syötä Maksuehdot-kenttään maksuehtokentän tunnus.</span><span class="sxs-lookup"><span data-stu-id="9d765-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="9d765-127">Syötä Kuvaus-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="9d765-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="9d765-128">Valitse maksutapa, kuten postiennakko, netto, nykyinen kuukausi jne.</span><span class="sxs-lookup"><span data-stu-id="9d765-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="9d765-129">Maksuehtoa käytetään erääntymisen laskennan aloittamisen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="9d765-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="9d765-130">Esimerkiksi Netto-kohtaa käytetään, jos eräpäivä on aina tietty laskupäivämäärän jälkeisten kuukausien tai päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="9d765-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="9d765-131">Postiennakko-kohtaa käytetään, kun maksu vaaditaan laskun yhteydessä. Tällöin eräpäivää ei voida laskea.</span><span class="sxs-lookup"><span data-stu-id="9d765-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="9d765-132">Valitaan tässä tehtävän ohjauksessa Nykyinen kuukausi.</span><span class="sxs-lookup"><span data-stu-id="9d765-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="9d765-133">Valitse maksupäivä, jos laskennassa tarvitaan tiettyä viikonpäivää tai päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="9d765-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="9d765-134">Voit syöttää määrän maksuehdoista riippuen kuukausina tai päivinä.</span><span class="sxs-lookup"><span data-stu-id="9d765-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="9d765-135">Voit myös käyttää maksusuunnitelmaa tai maksupäivää tehdessäsi lisäyksen maksutavan loppuun.</span><span class="sxs-lookup"><span data-stu-id="9d765-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="9d765-136">Jos eräpäivä on aina seuraavan kuukauden 10. päivä, valitse maksupäiväksi 10. päivä.</span><span class="sxs-lookup"><span data-stu-id="9d765-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="9d765-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d765-137">Click Save.</span></span>
16. <span data-ttu-id="9d765-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9d765-138">Close the page.</span></span>
17. <span data-ttu-id="9d765-139">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Käteisalennukset.</span><span class="sxs-lookup"><span data-stu-id="9d765-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="9d765-140">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9d765-140">Click New.</span></span>
    * <span data-ttu-id="9d765-141">Tällä sivulla määritetään, miten käteisalennus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="9d765-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="9d765-142">Syötä Käteisalennus-kenttään käteisalennuskentän tunnus.</span><span class="sxs-lookup"><span data-stu-id="9d765-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="9d765-143">Syötä Kuvaus-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="9d765-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="9d765-144">Jos käytettävissä on käteisalennustasoja, valitse tämän uuden käteisalennuksen jälkeen soveltuva seuraava alennuskoodi.</span><span class="sxs-lookup"><span data-stu-id="9d765-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="9d765-145">Syötä käteisalennuksen päivämäärän laskennassa käytettävien päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="9d765-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="9d765-146">Jos valittuna on Nettoperiaate, päivien määrä lisätään laskupäivämäärään, kun käteisalennuksen päivämäärä lasketaan.</span><span class="sxs-lookup"><span data-stu-id="9d765-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="9d765-147">Anna käteisalennuksen prosentti.</span><span class="sxs-lookup"><span data-stu-id="9d765-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="9d765-148">Syötä päätili, jolle myyntilaskujen käteisalennus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9d765-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="9d765-149">Valitse vaihtoehto Alennuksen vastatilit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="9d765-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="9d765-150">Jos valitset Laskurivien tilit -kohdan, käteisalennus kirjataan samalle toimittajan laskun käyttöomaisuuserän/kulujen päätilille.</span><span class="sxs-lookup"><span data-stu-id="9d765-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="9d765-151">Jos valitset Käytä toimittajan laskuissa päätiliä -kohdan, käteisalennus kirjataan Toimittajan laskujen päätili -kohdassa määritetylle päätilille.</span><span class="sxs-lookup"><span data-stu-id="9d765-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="9d765-152">Tässä esimerkissä valitaan Käytä toimittajan laskuissa päätiliä.</span><span class="sxs-lookup"><span data-stu-id="9d765-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="9d765-153">Syötä päätili, jolle toimittajan laskujen käteisalennus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9d765-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="9d765-154">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9d765-154">Click Save.</span></span>


