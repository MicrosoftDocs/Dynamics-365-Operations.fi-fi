--- 
title: "Rekisteröi myyntiprovisiot"
description: "Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d21f9047dcea0af59c24339ebb57e8eabe3950d4
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="22404-103">Rekisteröi myyntiprovisiot</span><span class="sxs-lookup"><span data-stu-id="22404-103">Register sales commissions</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22404-104">Tässä menettelyssä käsitellään, miten myyntiprovisiot lasketaan ja rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="22404-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="22404-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="22404-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="22404-106">Suorita ennen tämän opastuksen aloittamista Määritä myyntikomission säännöt -opastus ja varmista, että sinulla on kaikki tarvittavat komissiolaskelma-asetukset.</span><span class="sxs-lookup"><span data-stu-id="22404-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="22404-107">Kirjaa muistiin asiakasnumerot ja nimiketunnukset, jotka olevat valinnut provisioprosessiin, ja luo niillä pyydettäessä myyntitilaus tässä opastuksessa.</span><span class="sxs-lookup"><span data-stu-id="22404-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="22404-108">Laskuta myyntitilaus, josta myyjä saa provision</span><span class="sxs-lookup"><span data-stu-id="22404-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="22404-109">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="22404-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="22404-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="22404-110">Click New.</span></span>
3. <span data-ttu-id="22404-111">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="22404-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="22404-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="22404-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="22404-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="22404-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="22404-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22404-114">Click OK.</span></span>
7. <span data-ttu-id="22404-115">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="22404-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="22404-116">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="22404-116">Click Change view.</span></span>
9. <span data-ttu-id="22404-117">Valitse Otsikkonäkymä.</span><span class="sxs-lookup"><span data-stu-id="22404-117">Click Header view.</span></span>
10. <span data-ttu-id="22404-118">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="22404-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="22404-119">Myyntiryhmä-kentän arvo vastaa ryhmää, johon on määritetty vähintään yksi myyntiedustaja.</span><span class="sxs-lookup"><span data-stu-id="22404-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="22404-120">Ryhmän jäsenet saavat provisiot ennalta määritettyjen prosenttien ja jaon mukaisesti, kun tilaus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="22404-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="22404-121">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="22404-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="22404-122">Myös myyntiryhmä kopioidaan myyntitilausriville.</span><span class="sxs-lookup"><span data-stu-id="22404-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="22404-123">Voit muuttaa sitä niin, että se poikkeaa otsikon ja/tai rivien välisestä ryhmästä.</span><span class="sxs-lookup"><span data-stu-id="22404-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="22404-124">Provisioryhmä-kentän arvo vastaa ryhmää, jonka olet luonut vähintään yhdelle asiakkaille provisioiden seurantaa varten.</span><span class="sxs-lookup"><span data-stu-id="22404-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="22404-125">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="22404-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="22404-126">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="22404-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="22404-127">Valitse Vaihda näkymä.</span><span class="sxs-lookup"><span data-stu-id="22404-127">Click Change view.</span></span>
13. <span data-ttu-id="22404-128">Valitse Rivinäkymä.</span><span class="sxs-lookup"><span data-stu-id="22404-128">Click Line view.</span></span>
14. <span data-ttu-id="22404-129">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="22404-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="22404-130">Valitse luettelosta provisioille määritetty nimike.</span><span class="sxs-lookup"><span data-stu-id="22404-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="22404-131">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="22404-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="22404-132">Kirjoita rivin nettosumma muistiin.</span><span class="sxs-lookup"><span data-stu-id="22404-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="22404-133">Se vastaa myyntituottoa, joka on tässä esimerkissä provisiolaskelman peruste.</span><span class="sxs-lookup"><span data-stu-id="22404-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="22404-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="22404-134">Click Save.</span></span>
18. <span data-ttu-id="22404-135">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="22404-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="22404-136">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="22404-136">Click Invoice.</span></span>
20. <span data-ttu-id="22404-137">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="22404-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="22404-138">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="22404-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="22404-139">Valitse Kirjaus-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="22404-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="22404-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22404-140">Click OK.</span></span>
24. <span data-ttu-id="22404-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="22404-141">Click OK.</span></span>
    * <span data-ttu-id="22404-142">Tapahtuman kirjaaminen kestää noin minuutin.</span><span class="sxs-lookup"><span data-stu-id="22404-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="22404-143">Anna käsittelyn valmistua äläkä sulje sivua.</span><span class="sxs-lookup"><span data-stu-id="22404-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="22404-144">Tarkastele rekisteröityjä myyntiprovisioita</span><span class="sxs-lookup"><span data-stu-id="22404-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="22404-145">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="22404-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="22404-146">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="22404-146">Click Invoice.</span></span>
3. <span data-ttu-id="22404-147">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="22404-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="22404-148">Valitse Provisiotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="22404-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="22404-149">Yhteenveto-välilehti sisältää rivit, jotka vastaavat laskutettuun myyntitilaukseen liitetyille myyntiedustajille maksettavia provisiosummia.</span><span class="sxs-lookup"><span data-stu-id="22404-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="22404-150">Tarkastellaan tietoja tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="22404-150">Let's review the details.</span></span>     
    * <span data-ttu-id="22404-151">Jos määritit Provisiomyynti-ryhmän Määritä myyntiprovision säännöt -opastuksessa, kaksi myyjää saa myyntiprovisioita ja provisio jaetaan tasan heidän keskeen.</span><span class="sxs-lookup"><span data-stu-id="22404-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="22404-152">Tässä esimerkissä provision kokonaismäärä lasketaan myyntituoton prosenttiosuutena (tilausrivin nettosumma).</span><span class="sxs-lookup"><span data-stu-id="22404-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="22404-153">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="22404-153">Close the page.</span></span>
6. <span data-ttu-id="22404-154">Valitse Tosite.</span><span class="sxs-lookup"><span data-stu-id="22404-154">Click Voucher.</span></span>
    * <span data-ttu-id="22404-155">Voit tarkastella esimääritetyille provision kulu- ja ostoreskontratileille kirjattujen provisiosummien tositetapahtumia.</span><span class="sxs-lookup"><span data-stu-id="22404-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


