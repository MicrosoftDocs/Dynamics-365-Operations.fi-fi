--- 
title: Luo tekstimuotoinen lasku
description: "Tässä artikkelissa näytetään miten tekstimuotoinen myyntilasku luodaan."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
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
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="2c8c2-103">Luo tekstimuotoinen lasku</span><span class="sxs-lookup"><span data-stu-id="2c8c2-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c8c2-104">Tässä artikkelissa näytetään miten tekstimuotoinen myyntilasku luodaan.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="2c8c2-105">Tässä menettelyssä käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="2c8c2-106">Luo tekstimuotoinen lasku</span><span class="sxs-lookup"><span data-stu-id="2c8c2-106">Create a free text invoice</span></span>

1. <span data-ttu-id="2c8c2-107">Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2c8c2-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-108">Click New.</span></span>
3. <span data-ttu-id="2c8c2-109">Valitse arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="2c8c2-110">Laskutustili on oletusarvoisesti sama kuin asiakastili.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="2c8c2-111">Kirjanpidon tila alkaa Käsittelyssä-tilasta, jos laskua ei ole kirjattu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="2c8c2-112">Laskunumero liitetään, kun lasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="2c8c2-113">Kun käytössä ovat SEPA-valtakirjat, suoraveloitusvaltakirja täytetään automaattisesti asiakastilin valinnan yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="2c8c2-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2c8c2-115">Määritä Päätili-kenttään tilinumero ilman dimensioita.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="2c8c2-116">Voit myös syöttää päätilille yhden tai useamman merkin ja käyttää valintaa etsiessäsi tiliä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="2c8c2-117">Dimensiot syötetään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="2c8c2-118">Laajenna Rivin tiedot -pikavälilehti niin, että voit lisätä päätilille dimensioita.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="2c8c2-119">Valitse Taloushallinnon dimensiot -välilehti.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="2c8c2-120">Dimensiot kuuluvat vain valitulle riville.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="2c8c2-121">Arvonlisäveroryhmän tiedot täytetään asiakkaan tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="2c8c2-122">Jos asiakkaalla ei ole arvonlisäveroryhmää, käytetään päätilin arvonlisäveroryhmää.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="2c8c2-123">Nimikkeiden arvonlisäveroryhmän tiedot täytetään päätilin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="2c8c2-124">Jos päätilillä ei ole nimikkeen arvonlisäveroryhmää, käytetään kirjanpidon arvolisäveroparametrin nimikkeen arvonlisäveroryhmää.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="2c8c2-125">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2c8c2-126">Määrä on valinnainen tieto.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="2c8c2-127">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2c8c2-128">Yksikköhinta on valinnainen tieto.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="2c8c2-129">Summa lasketaan kertomalla määrä yksikköhinnalla.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2c8c2-130">Voit kuitenkin ohittaa laskennan ja syöttää summan.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="2c8c2-131">Tarkastele laskulle laskettua arvonlisäveroa valitsemalla Arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="2c8c2-132">Voit tarkastella tämän sivun arvonlisäverosummia tai korvata summat Oikaisu-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="2c8c2-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-133">Click OK.</span></span>
12. <span data-ttu-id="2c8c2-134">Lisää laskuun kulu valitsemalla Kulut.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="2c8c2-135">Kirjoita Kulujen koodi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="2c8c2-136">Syötä Kulujen arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="2c8c2-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-137">Close the page.</span></span>
16. <span data-ttu-id="2c8c2-138">Tarkastele yhteenvetolaskun tietoja ja summia valitsemalla Summat.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="2c8c2-139">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-139">Click Close.</span></span>
18. <span data-ttu-id="2c8c2-140">Kirjaa lasku valitsemalla Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-140">Click Post to post the invoice.</span></span> <span data-ttu-id="2c8c2-141">Voit peruuttaa toiminnon ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="2c8c2-142">Voit muuttaa laskun tulostamisen aikataulua seuraavasti: Tulosta kukin lasku päivityksen yhteydessä valitsemalla Nykyinen, tai tulosta vasta kaikkien laskujen päivityksen jälkeen valitsemalla Jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="2c8c2-143">Jos haluat muuttaa asiakkaan luottorajan ennen kirjaamista tapahtuvaa tarkistustapaa, muuta luottorajatyyppiä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="2c8c2-144">Jos haluat tulostaa laskun, valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="2c8c2-145">Jos haluat kirjata laskun, valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="2c8c2-146">Voit tulostaa laskun ilman kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="2c8c2-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="2c8c2-148">Kopioi rivit</span><span class="sxs-lookup"><span data-stu-id="2c8c2-148">Copy lines</span></span>
<span data-ttu-id="2c8c2-149">Valitse vähintään yksi rivi vapaatekstilaskun riveille ja valitse Kopioi valitut rivit.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="2c8c2-150">Voit määrittää montako kopiota haluat tehdä ja myös kopioida ilmoituksia ja liitteitä.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="2c8c2-151">Voit kopioida jakoja tai sallia niiden uudelleenluonnin, kun kirjaat.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="2c8c2-152">Kun kopioit rivejä, voit muokata tietoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="2c8c2-153">Luo vapaatekstilasku mallin mukaan</span><span class="sxs-lookup"><span data-stu-id="2c8c2-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="2c8c2-154">Voit luoda vapaatekstilaskun mallin mukaan.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="2c8c2-155">Kun valitset Uusi Lasku-välilehden templaateista, voit valita templaatin nimen ja uuden tekstimuotoisen laskun asiakastilin.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="2c8c2-156">Voit valita oletusarvot, kuten maksuehdot ja maksutapa asiakkaan mukaan tai arvoja, jotka on tallennettu malliin.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="2c8c2-157">Uusi vapaatekstilasku luodaan ja voit muokata tämän laskun arvoja.</span><span class="sxs-lookup"><span data-stu-id="2c8c2-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


