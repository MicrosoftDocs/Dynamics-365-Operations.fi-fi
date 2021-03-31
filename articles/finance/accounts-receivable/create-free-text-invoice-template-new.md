---
title: Luo vapaatekstilaskumalli
description: Tässä menettelyssä näytetään miten luodaan vapaan tekstin laskumalli.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdcb307686800e0038212982c1eac6f1c14cf8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217479"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="c8903-103">Luo vapaatekstilaskumalli</span><span class="sxs-lookup"><span data-stu-id="c8903-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8903-104">Tässä esittelyssä käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="c8903-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="c8903-105">Menettely on tarkoitettu käyttäjälle, joka on vastuussa myyntireskontran laskujen hallinnasta ja käsittelemisestä.</span><span class="sxs-lookup"><span data-stu-id="c8903-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="c8903-106">Luo malli</span><span class="sxs-lookup"><span data-stu-id="c8903-106">Create a template</span></span>

1. <span data-ttu-id="c8903-107">Siirry kohtaan Myyntireskontra > Laskut > Toistuvat laskut > Vapaatekstilaskun mallit.</span><span class="sxs-lookup"><span data-stu-id="c8903-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="c8903-108">Tämän lomakkeen avulla voit luoda vapaatekstilaskun malleja, jotka sisältävät laskurivejä, veloituksia, kirjanpidollisen jaon mallin ja kirjanpitotilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="c8903-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="c8903-109">Luo uusi vapaatekstilaskun malli valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="c8903-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="c8903-110">Syötä Mallin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c8903-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="c8903-111">Mallin nimi yksilöi vapaatekstilaskun mallin.</span><span class="sxs-lookup"><span data-stu-id="c8903-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="c8903-112">Kahdelle mallille ei voi määrittää samaa mallin nimeä.</span><span class="sxs-lookup"><span data-stu-id="c8903-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="c8903-113">Syötä Kuvaus-kenttään mallin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c8903-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="c8903-114">Laajenna Laskurivit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c8903-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="c8903-115">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c8903-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="c8903-116">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="c8903-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c8903-117">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c8903-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="c8903-118">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c8903-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8903-119">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="c8903-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="c8903-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c8903-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c8903-121">Valitse Nimikkeen veroryhmä -kentässä nykyisen laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="c8903-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="c8903-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c8903-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c8903-123">Syötä Yksikköhinta-kenttään laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="c8903-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="c8903-124">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="c8903-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="c8903-125">Lisää vapaatekstilaskun malliin uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="c8903-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="c8903-126">Kirjoita Kuvaus-kenttään laskurivin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c8903-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="c8903-127">Valitse Päätili-kentässä tuottotili.</span><span class="sxs-lookup"><span data-stu-id="c8903-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c8903-128">Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle Asiakkaan kirjausprofiilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c8903-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="c8903-129">Avaa haku valitsemalla Arvonlisäveroryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c8903-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8903-130">Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="c8903-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="c8903-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c8903-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c8903-132">Avaa haku valitsemalla Nimikkeen arvonlisäveroryhmä -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c8903-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8903-133">Valitun laskurivin nimikkeen arvonlisäveroryhmä.</span><span class="sxs-lookup"><span data-stu-id="c8903-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="c8903-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c8903-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c8903-135">Yksiköiden määrän syöttäminen laskuriville tai määrän tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="c8903-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="c8903-136">Tämä numero kerrotaan Yksikköhinta-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="c8903-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="c8903-137">Syötä laskurivin yksikkökohtainen hinta tai tarkastele sitä.</span><span class="sxs-lookup"><span data-stu-id="c8903-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="c8903-138">Tämä summa kerrotaan Määrä-kentän arvolla laskurivin summan määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="c8903-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="c8903-139">Tarkastele ja muokkaa yksittäisen rivin ja alatason rivien kirjanpidollisia jakoja.</span><span class="sxs-lookup"><span data-stu-id="c8903-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="c8903-140">Kirjanpidolliset jaot määrittävät, miten summa käsitellään, esimerkiksi miten tuotto, vero tai maksu käsitellään vapaatekstilaskussa.</span><span class="sxs-lookup"><span data-stu-id="c8903-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="c8903-141">Päivitä valitun laskurivin kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="c8903-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="c8903-142">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="c8903-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="c8903-143">Tallenna vapaatekstilaskumalli</span><span class="sxs-lookup"><span data-stu-id="c8903-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="c8903-144">Voit myös tallentaa aiemman vapaatekstilaskun mallina.</span><span class="sxs-lookup"><span data-stu-id="c8903-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="c8903-145">Kun valitset Tallenna malliin Lasku-välilehdellä, anna sille nimi ja liitä mallin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="c8903-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="c8903-146">Jos mallin nimi on jo käytössä, näyttöön tulee ilmoitus, että malli on jo olemassa.</span><span class="sxs-lookup"><span data-stu-id="c8903-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="c8903-147">Voit kuitenkin napsauttaa Ok ja korvata sen.</span><span class="sxs-lookup"><span data-stu-id="c8903-147">You can still click on Ok to replace it.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]