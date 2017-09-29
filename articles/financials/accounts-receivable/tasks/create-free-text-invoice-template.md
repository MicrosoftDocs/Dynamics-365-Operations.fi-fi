--- 
title: Luo vapaatekstilaskumalli
description: "Tässä tallenteessa käytetään esittely-yritystä USMF."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="b0d11-103">Luo vapaatekstilaskumalli</span><span class="sxs-lookup"><span data-stu-id="b0d11-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0d11-104">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="b0d11-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="b0d11-105">Tallennus on tarkoitettu käyttäjälle, joka on vastuussa myyntireskontran laskujen hallinnasta ja käsittelemisestä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="b0d11-106">Siirry kohtaan Myyntireskontra > Laskut > Toistuvat laskut > Vapaatekstilaskun mallit.</span><span class="sxs-lookup"><span data-stu-id="b0d11-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="b0d11-107">Tämän lomakkeen avulla voit luoda vapaatekstilaskun malleja, jotka sisältävät laskurivejä, veloituksia, kirjanpidollisen jaon mallin ja kirjanpitotilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="b0d11-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="b0d11-108">Luo uusi vapaatekstilaskun malli valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="b0d11-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="b0d11-109">Syötä Mallin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b0d11-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="b0d11-110">Mallin nimi yksilöi vapaatekstilaskun mallin.</span><span class="sxs-lookup"><span data-stu-id="b0d11-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="b0d11-111">Kahdelle mallille ei voi määrittää samaa mallin nimeä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="b0d11-112">Syötä Kuvaus-kenttään mallin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b0d11-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="b0d11-113">Laajenna Laskurivit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b0d11-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="b0d11-114">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b0d11-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="b0d11-115">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="b0d11-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="b0d11-116">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b0d11-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="b0d11-117">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b0d11-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b0d11-118">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="b0d11-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b0d11-120">Valitse Nimikkeen veroryhmä -kentässä nykyisen laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="b0d11-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b0d11-122">Syötä Yksikköhinta-kenttään laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="b0d11-123">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b0d11-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="b0d11-124">Lisää vapaatekstilaskun malliin uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="b0d11-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="b0d11-125">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b0d11-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="b0d11-126">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="b0d11-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="b0d11-127">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b0d11-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="b0d11-128">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b0d11-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b0d11-129">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="b0d11-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b0d11-131">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b0d11-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b0d11-132">Valitun laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="b0d11-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b0d11-134">Yksiköiden määrän syöttäminen laskuriville tai määrän tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="b0d11-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="b0d11-135">Tämä numero kerrotaan Yksikköhinta-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b0d11-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="b0d11-136">Syötä laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="b0d11-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="b0d11-137">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="b0d11-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="b0d11-138">Tarkastele ja muokkaa yksittäisen rivin ja alatason rivien kirjanpidollisia jakoja.</span><span class="sxs-lookup"><span data-stu-id="b0d11-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="b0d11-139">Kirjanpidolliset jaot määrittävät, miten summa käsitellään, esimerkiksi miten tuotto, vero tai maksu käsitellään vapaatekstilaskussa.</span><span class="sxs-lookup"><span data-stu-id="b0d11-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="b0d11-140">Päivitä valitun laskurivin kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="b0d11-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="b0d11-141">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="b0d11-141">Click Close.</span></span>


