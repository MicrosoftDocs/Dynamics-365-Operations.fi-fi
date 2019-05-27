---
title: Rekisteröi myyntiprovisiot
description: Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560709"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="3174e-103">Rekisteröi myyntiprovisiot</span><span class="sxs-lookup"><span data-stu-id="3174e-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3174e-104">Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="3174e-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="3174e-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="3174e-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="3174e-106">Suorita ennen tämän opastuksen aloittamista Määritä myyntikomission säännöt -opastus ja varmista, että sinulla on kaikki tarvittavat komissiolaskelma-asetukset.</span><span class="sxs-lookup"><span data-stu-id="3174e-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="3174e-107">Kirjaa muistiin asiakasnumerot ja nimiketunnukset, jotka olevat valinnut provisioprosessiin, ja luo niillä pyydettäessä myyntitilaus tässä opastuksessa.</span><span class="sxs-lookup"><span data-stu-id="3174e-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="3174e-108">Laskuta myyntitilaus, josta myyjä saa provision</span><span class="sxs-lookup"><span data-stu-id="3174e-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="3174e-109">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="3174e-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="3174e-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3174e-110">Click New.</span></span>
3. <span data-ttu-id="3174e-111">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3174e-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3174e-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3174e-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3174e-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3174e-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3174e-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3174e-114">Click OK.</span></span>
7. <span data-ttu-id="3174e-115">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="3174e-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="3174e-116">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="3174e-116">Click Change view.</span></span>
9. <span data-ttu-id="3174e-117">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="3174e-117">Click Header view.</span></span>
10. <span data-ttu-id="3174e-118">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="3174e-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="3174e-119">Myyntiryhmä-kentän arvo vastaa ryhmää, johon on määritetty vähintään yksi myyntiedustaja.</span><span class="sxs-lookup"><span data-stu-id="3174e-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="3174e-120">Ryhmän jäsenet saavat provisiot ennalta määritettyjen prosenttien ja jaon mukaisesti, kun tilaus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="3174e-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="3174e-121">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="3174e-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="3174e-122">Myös myyntiryhmä kopioidaan myyntitilausriville.</span><span class="sxs-lookup"><span data-stu-id="3174e-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="3174e-123">Voit muuttaa sitä niin, että se poikkeaa otsikon ja/tai rivien välisestä ryhmästä.</span><span class="sxs-lookup"><span data-stu-id="3174e-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="3174e-124">Provisioryhmä-kentän arvo vastaa ryhmää, jonka olet luonut vähintään yhdelle asiakkaille provisioiden seurantaa varten.</span><span class="sxs-lookup"><span data-stu-id="3174e-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="3174e-125">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="3174e-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="3174e-126">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="3174e-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="3174e-127">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="3174e-127">Click Change view.</span></span>
13. <span data-ttu-id="3174e-128">Valitse Rivinäkymä.</span><span class="sxs-lookup"><span data-stu-id="3174e-128">Click Line view.</span></span>
14. <span data-ttu-id="3174e-129">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3174e-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3174e-130">Valitse luettelosta provisioille määritetty nimike.</span><span class="sxs-lookup"><span data-stu-id="3174e-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="3174e-131">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3174e-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3174e-132">Kirjoita rivin nettosumma muistiin.</span><span class="sxs-lookup"><span data-stu-id="3174e-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="3174e-133">Se vastaa myyntituottoa, joka on tässä esimerkissä provisiolaskelman peruste.</span><span class="sxs-lookup"><span data-stu-id="3174e-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="3174e-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3174e-134">Click Save.</span></span>
18. <span data-ttu-id="3174e-135">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="3174e-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="3174e-136">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="3174e-136">Click Invoice.</span></span>
20. <span data-ttu-id="3174e-137">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="3174e-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="3174e-138">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="3174e-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="3174e-139">Valitse Kirjaus-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="3174e-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="3174e-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3174e-140">Click OK.</span></span>
24. <span data-ttu-id="3174e-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3174e-141">Click OK.</span></span>
    * <span data-ttu-id="3174e-142">Tapahtuman kirjaaminen kestää noin minuutin.</span><span class="sxs-lookup"><span data-stu-id="3174e-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="3174e-143">Anna käsittelyn valmistua äläkä sulje sivua.</span><span class="sxs-lookup"><span data-stu-id="3174e-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="3174e-144">Tarkastele rekisteröityjä myyntiprovisioita</span><span class="sxs-lookup"><span data-stu-id="3174e-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="3174e-145">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="3174e-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="3174e-146">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="3174e-146">Click Invoice.</span></span>
3. <span data-ttu-id="3174e-147">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="3174e-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="3174e-148">Valitse Provisiotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="3174e-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="3174e-149">Yhteenveto-välilehti sisältää rivit, jotka vastaavat laskutettuun myyntitilaukseen liitetyille myyntiedustajille maksettavia provisiosummia.</span><span class="sxs-lookup"><span data-stu-id="3174e-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="3174e-150">Tarkastellaan tietoja tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="3174e-150">Let's review the details.</span></span>     
    * <span data-ttu-id="3174e-151">Jos määritit Provisiomyynti-ryhmän Määritä myyntiprovision säännöt -opastuksessa, kaksi myyjää saa myyntiprovisioita ja provisio jaetaan tasan heidän keskeen.</span><span class="sxs-lookup"><span data-stu-id="3174e-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="3174e-152">Tässä esimerkissä provision kokonaismäärä lasketaan myyntituoton prosenttiosuutena (tilausrivin nettosumma).</span><span class="sxs-lookup"><span data-stu-id="3174e-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="3174e-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3174e-153">Close the page.</span></span>
6. <span data-ttu-id="3174e-154">Valitse Tosite.</span><span class="sxs-lookup"><span data-stu-id="3174e-154">Click Voucher.</span></span>
    * <span data-ttu-id="3174e-155">Voit tarkastella esimääritetyille provision kulu- ja ostoreskontratileille kirjattujen provisiosummien tositetapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3174e-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

