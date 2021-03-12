---
title: Luo tekstimuotoinen lasku
description: Tässä ohjeaiheessa käsitellään vapaatekstilaskuja.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991114"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="7652d-103">Luo tekstimuotoinen lasku</span><span class="sxs-lookup"><span data-stu-id="7652d-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7652d-104">Tässä ohjeaiheessa käsitellään vapaatekstilaskuja.</span><span class="sxs-lookup"><span data-stu-id="7652d-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="7652d-105">Tässä menettelyssä käytetään **USMF**-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="7652d-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="7652d-106">Luo tekstimuotoinen lasku</span><span class="sxs-lookup"><span data-stu-id="7652d-106">Create a free text invoice</span></span>

1. <span data-ttu-id="7652d-107">Siirry kohtaan **Myyntireskontra (tai Myynnin kirjanpito) \> Laskut \> Kaikki vapaatekstilaskut**.</span><span class="sxs-lookup"><span data-stu-id="7652d-107">Go to **Accounts receivable (or Sales Ledger) \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="7652d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7652d-108">Select **New**.</span></span>
3. <span data-ttu-id="7652d-109">Valitse arvo **Asiakastili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7652d-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="7652d-110">Asiakastiliksi valittua tiliä käytetään oletusarvoisesti laskutustilinä.</span><span class="sxs-lookup"><span data-stu-id="7652d-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="7652d-111">Jos laskua ei ole kirjattu, kirjanpidon tila alkaa **Käsittelyssä**-tilasta.</span><span class="sxs-lookup"><span data-stu-id="7652d-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="7652d-112">Laskunumero liitetään, kun lasku on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="7652d-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="7652d-113">Kun käytössä on SEPA-valtakirjat, suoraveloitusvaltakirja annetaan automaattisesti asiakastilin valinnan yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7652d-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="7652d-114">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7652d-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="7652d-115">Määritä **Päätili**-kenttään tilinumero, jolla ei ole dimensioita.</span><span class="sxs-lookup"><span data-stu-id="7652d-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="7652d-116">Dimensioiden antaminen käsitellään myöhemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="7652d-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="7652d-117">Voit kirjoittaa myös vähintään yhden päätilin merkin ja käyttää valintaa etsiessäsi tiliä.</span><span class="sxs-lookup"><span data-stu-id="7652d-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="7652d-118">Lisää dimensiot päätiliin valitsemalla **Rivin tiedot** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="7652d-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="7652d-119">Valitse **Taloushallinnon dimensiot** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="7652d-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="7652d-120">Dimensiot kuuluvat vain valitulle riville.</span><span class="sxs-lookup"><span data-stu-id="7652d-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="7652d-121">Arvonlisäveroryhmä täytetään asiakkaan tiedoista.</span><span class="sxs-lookup"><span data-stu-id="7652d-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="7652d-122">Jos asiakkaalla ei ole arvonlisäveroryhmää, käytetään päätilin arvonlisäveroryhmää.</span><span class="sxs-lookup"><span data-stu-id="7652d-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="7652d-123">Nimikkeiden arvonlisäveroryhmän tiedot täytetään päätilin tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="7652d-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="7652d-124">Jos päätilillä ei ole nimikkeen arvonlisäveroryhmää, käytetään sitä nimikkeen arvonlisäveroryhmää, joka on määritetty kirjanpidon arvolisäveroparametreissa.</span><span class="sxs-lookup"><span data-stu-id="7652d-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="7652d-125">Valinnainen: Anna luku **Määrä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7652d-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="7652d-126">Valinnainen: Anna luku **Yksikköhinta**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7652d-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="7652d-127">Summa lasketaan kertomalla määrä yksikköhinnalla.</span><span class="sxs-lookup"><span data-stu-id="7652d-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="7652d-128">Voit kuitenkin ohittaa laskennan ja antaa summan.</span><span class="sxs-lookup"><span data-stu-id="7652d-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="7652d-129">Tarkastele laskulle laskettua arvonlisäveroa valitsemalla **Arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="7652d-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="7652d-130">Voit tarkastella tämän sivun arvonlisäverosummia tai korvata summat **Oikaisu**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7652d-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="7652d-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7652d-131">Select **OK**.</span></span>
12. <span data-ttu-id="7652d-132">Lisää laskuun kulu valitsemalla **Kulut**.</span><span class="sxs-lookup"><span data-stu-id="7652d-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="7652d-133">Kirjoita **Kulujen koodi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7652d-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="7652d-134">Kirjoita **Kulujen arvo** -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="7652d-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="7652d-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7652d-135">Close the page.</span></span>
16. <span data-ttu-id="7652d-136">Tarkastele yhteenvetolaskun tietoja ja summia valitsemalla **Summat**.</span><span class="sxs-lookup"><span data-stu-id="7652d-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="7652d-137">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="7652d-137">Select **Close**.</span></span>
18. <span data-ttu-id="7652d-138">Kirjaa lasku valitsemalla **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="7652d-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="7652d-139">Peruutus on edelleen mahdollista ennen varsinaista kirjausta.</span><span class="sxs-lookup"><span data-stu-id="7652d-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="7652d-140">Voit muuttaa laskun tulostamisen aikataulua.</span><span class="sxs-lookup"><span data-stu-id="7652d-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="7652d-141">Tulosta kukin lasku päivityksen yhteydessä valitsemalla **Nykyinen**.</span><span class="sxs-lookup"><span data-stu-id="7652d-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="7652d-142">Tulosta vasta kaikkien laskujen päivityksen jälkeen valitsemalla **Jälkeen**.</span><span class="sxs-lookup"><span data-stu-id="7652d-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="7652d-143">Voit muuttaa tapaa, jolla asiakkaan luottoraja tarkistetaan ennen laskun kirjausta, muuttamalla **Luottorajatyyppi**-kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="7652d-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="7652d-144">Voit tulostaa laskun, jos valitset **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7652d-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="7652d-145">Voit kirjata laskun, jos valitset **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7652d-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="7652d-146">Voit tulostaa laskun ilman, että se kirjataan.</span><span class="sxs-lookup"><span data-stu-id="7652d-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="7652d-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7652d-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="7652d-148">Kopioi rivit</span><span class="sxs-lookup"><span data-stu-id="7652d-148">Copy lines</span></span>
<span data-ttu-id="7652d-149">Valitse vähintään yksi rivi vapaatekstilaskun riveille ja valitse sitten **Kopioi valitut rivit**.</span><span class="sxs-lookup"><span data-stu-id="7652d-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="7652d-150">Voit määrittää kopioiden määrän. Voit kopioida ilmoituksia ja liitteitä.</span><span class="sxs-lookup"><span data-stu-id="7652d-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="7652d-151">Voit joko kopioida jakelun tai sallia niiden uudelleenluonnin kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7652d-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="7652d-152">Kun olet kopioinut rivit, voit muokata tietoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7652d-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="7652d-153">Luo vapaatekstilasku mallin mukaan</span><span class="sxs-lookup"><span data-stu-id="7652d-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="7652d-154">Voit luoda vapaatekstilaskun mallin mukaan.</span><span class="sxs-lookup"><span data-stu-id="7652d-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="7652d-155">Kun valitset **Uusi mallista** **Lasku**-välilehdessä, voit valita mallin nimen ja uuden tekstimuotoisen laskun asiakastilin.</span><span class="sxs-lookup"><span data-stu-id="7652d-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="7652d-156">Oletusarvot, kuten maksuehdot ja maksutapa, voidaan automaattisesti täyttää asiakkaan tiedoista, tai voit käyttää arvoja, jotka on tallennettu malliin.</span><span class="sxs-lookup"><span data-stu-id="7652d-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="7652d-157">Uusi vapaatekstilasku luodaan ja voit muokata sen arvoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7652d-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
