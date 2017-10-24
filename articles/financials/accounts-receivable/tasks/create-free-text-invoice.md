--- 
title: Luo tekstimuotoinen lasku
description: "Tässä tehtävän ohjauksessa kerrotaan, miten vapaatekstilasku luodaan."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="51268-103">Luo tekstimuotoinen lasku</span><span class="sxs-lookup"><span data-stu-id="51268-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51268-104">Tässä tehtävän ohjauksessa kerrotaan, miten vapaatekstilasku luodaan.</span><span class="sxs-lookup"><span data-stu-id="51268-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="51268-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="51268-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="51268-106">Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.</span><span class="sxs-lookup"><span data-stu-id="51268-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="51268-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="51268-107">Click New.</span></span>
3. <span data-ttu-id="51268-108">Valitse arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="51268-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="51268-109">Laskutustili on oletusarvoisesti sama kuin asiakastili.</span><span class="sxs-lookup"><span data-stu-id="51268-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="51268-110">Kirjanpidon tila alkaa Käsittelyssä-tilasta, jos laskua ei ole kirjattu.</span><span class="sxs-lookup"><span data-stu-id="51268-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="51268-111">Laskunumero liitetään, kun lasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="51268-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="51268-112">Kun käytössä ovat SEPA-valtakirjat, suoraveloitusvaltakirja täytetään automaattisesti asiakastilin valinnan yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="51268-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="51268-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="51268-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="51268-114">Määritä Päätili-kenttään tilinumero ilman dimensioita.</span><span class="sxs-lookup"><span data-stu-id="51268-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="51268-115">Voit myös syöttää päätilille yhden tai useamman merkin ja käyttää valintaa etsiessäsi tiliä.</span><span class="sxs-lookup"><span data-stu-id="51268-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="51268-116">Dimensiot syötetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="51268-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="51268-117">Laajenna Rivin tiedot -pikavälilehti niin, että voit lisätä päätilille dimensioita.</span><span class="sxs-lookup"><span data-stu-id="51268-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="51268-118">Valitse Taloushallinnon dimensiot -välilehti.</span><span class="sxs-lookup"><span data-stu-id="51268-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="51268-119">Dimensiot kuuluvat vain valitulle riville.</span><span class="sxs-lookup"><span data-stu-id="51268-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="51268-120">Arvonlisäveroryhmän tiedot täytetään asiakkaan tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="51268-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="51268-121">Jos asiakkaalla ei ole arvonlisäveroryhmää, käytetään päätilin arvonlisäveroryhmää.</span><span class="sxs-lookup"><span data-stu-id="51268-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="51268-122">Nimikkeiden arvonlisäveroryhmän tiedot täytetään päätilin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="51268-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="51268-123">Jos päätilillä ei ole nimikkeen arvonlisäveroryhmää, käytetään kirjanpidon arvolisäveroparametrin nimikkeen arvonlisäveroryhmää.</span><span class="sxs-lookup"><span data-stu-id="51268-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="51268-124">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="51268-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="51268-125">Määrä on valinnainen tieto.</span><span class="sxs-lookup"><span data-stu-id="51268-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="51268-126">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="51268-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="51268-127">Yksikköhinta on valinnainen tieto.</span><span class="sxs-lookup"><span data-stu-id="51268-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="51268-128">Summa lasketaan kertomalla määrä yksikköhinnalla.</span><span class="sxs-lookup"><span data-stu-id="51268-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="51268-129">Voit kuitenkin ohittaa laskennan ja syöttää summan.</span><span class="sxs-lookup"><span data-stu-id="51268-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="51268-130">Tarkastele laskulle laskettua arvonlisäveroa valitsemalla Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="51268-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="51268-131">Voit tarkastella tämän sivun arvonlisäverosummia tai korvata summat Oikaisu-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="51268-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="51268-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="51268-132">Click OK.</span></span>
12. <span data-ttu-id="51268-133">Lisää laskuun kulu valitsemalla Kulut.</span><span class="sxs-lookup"><span data-stu-id="51268-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="51268-134">Kirjoita Kulujen koodi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="51268-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="51268-135">Syötä Kulujen arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="51268-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="51268-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="51268-136">Close the page.</span></span>
16. <span data-ttu-id="51268-137">Tarkastele yhteenvetolaskun tietoja ja summia valitsemalla Summat.</span><span class="sxs-lookup"><span data-stu-id="51268-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="51268-138">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="51268-138">Click Close.</span></span>
18. <span data-ttu-id="51268-139">Kirjaa lasku valitsemalla Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="51268-139">Click Post to post the invoice.</span></span> <span data-ttu-id="51268-140">Voit peruuttaa toiminnon ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="51268-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="51268-141">Voit muuttaa laskun tulostamisen aikataulua seuraavasti: Tulosta kukin lasku päivityksen yhteydessä valitsemalla Nykyinen, tai tulosta vasta kaikkien laskujen päivityksen jälkeen valitsemalla Jälkeen.</span><span class="sxs-lookup"><span data-stu-id="51268-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="51268-142">Jos haluat muuttaa asiakkaan luottorajan ennen kirjaamista tapahtuvaa tarkistustapaa, muuta luottorajatyyppiä.</span><span class="sxs-lookup"><span data-stu-id="51268-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="51268-143">Jos haluat tulostaa laskun, valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="51268-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="51268-144">Jos haluat kirjata laskun, valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="51268-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="51268-145">Voit tulostaa laskun ilman kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="51268-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="51268-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="51268-146">Click OK.</span></span>


