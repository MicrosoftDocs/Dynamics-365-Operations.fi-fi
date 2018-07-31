--- 
title: Luo vapaatekstilaskumalli
description: "Tässä menettelyssä näytetään miten luodaan vapaan tekstin laskumalli."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
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
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 9b7ce8ba180f67c4a52439f4e03b59f07a71323d
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="516a0-103">Luo vapaatekstilaskumalli</span><span class="sxs-lookup"><span data-stu-id="516a0-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="516a0-104">Tässä esittelyssä käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="516a0-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="516a0-105">Menettely on tarkoitettu käyttäjälle, joka on vastuussa myyntireskontran laskujen hallinnasta ja käsittelemisestä.</span><span class="sxs-lookup"><span data-stu-id="516a0-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="516a0-106">Luo malli</span><span class="sxs-lookup"><span data-stu-id="516a0-106">Create a template</span></span>

1. <span data-ttu-id="516a0-107">Siirry kohtaan Myyntireskontra > Laskut > Toistuvat laskut > Vapaatekstilaskun mallit.</span><span class="sxs-lookup"><span data-stu-id="516a0-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="516a0-108">Tämän lomakkeen avulla voit luoda vapaatekstilaskun malleja, jotka sisältävät laskurivejä, veloituksia, kirjanpidollisen jaon mallin ja kirjanpitotilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="516a0-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="516a0-109">Luo uusi vapaatekstilaskun malli valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="516a0-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="516a0-110">Syötä Mallin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="516a0-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="516a0-111">Mallin nimi yksilöi vapaatekstilaskun mallin.</span><span class="sxs-lookup"><span data-stu-id="516a0-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="516a0-112">Kahdelle mallille ei voi määrittää samaa mallin nimeä.</span><span class="sxs-lookup"><span data-stu-id="516a0-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="516a0-113">Syötä Kuvaus-kenttään mallin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="516a0-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="516a0-114">Laajenna Laskurivit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="516a0-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="516a0-115">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="516a0-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="516a0-116">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="516a0-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="516a0-117">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="516a0-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="516a0-118">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="516a0-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="516a0-119">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="516a0-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="516a0-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="516a0-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="516a0-121">Valitse Nimikkeen veroryhmä -kentässä nykyisen laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="516a0-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="516a0-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="516a0-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="516a0-123">Syötä Yksikköhinta-kenttään laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="516a0-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="516a0-124">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="516a0-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="516a0-125">Lisää vapaatekstilaskun malliin uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="516a0-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="516a0-126">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="516a0-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="516a0-127">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="516a0-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="516a0-128">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="516a0-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="516a0-129">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="516a0-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="516a0-130">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="516a0-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="516a0-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="516a0-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="516a0-132">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="516a0-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="516a0-133">Valitun laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="516a0-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="516a0-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="516a0-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="516a0-135">Yksiköiden määrän syöttäminen laskuriville tai määrän tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="516a0-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="516a0-136">Tämä numero kerrotaan Yksikköhinta-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="516a0-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="516a0-137">Syötä laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="516a0-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="516a0-138">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="516a0-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="516a0-139">Tarkastele ja muokkaa yksittäisen rivin ja alatason rivien kirjanpidollisia jakoja.</span><span class="sxs-lookup"><span data-stu-id="516a0-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="516a0-140">Kirjanpidolliset jaot määrittävät, miten summa käsitellään, esimerkiksi miten tuotto, vero tai maksu käsitellään vapaatekstilaskussa.</span><span class="sxs-lookup"><span data-stu-id="516a0-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="516a0-141">Päivitä valitun laskurivin kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="516a0-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="516a0-142">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="516a0-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="516a0-143">Tallenna vapaatekstilaskumalli</span><span class="sxs-lookup"><span data-stu-id="516a0-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="516a0-144">Voit myös tallentaa aiemman vapaatekstilaskun mallina.</span><span class="sxs-lookup"><span data-stu-id="516a0-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="516a0-145">Kun valitset Tallenna malliin Lasku-välilehdellä, anna sille nimi ja liitä mallin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="516a0-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="516a0-146">Jos mallin nimi on jo käytössä, näyttöön tulee ilmoitus, että malli on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="516a0-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="516a0-147">Voit kuitenkin napsauttaa Ok ja korvata sen.</span><span class="sxs-lookup"><span data-stu-id="516a0-147">You can still click on Ok to replace it.</span></span> 

