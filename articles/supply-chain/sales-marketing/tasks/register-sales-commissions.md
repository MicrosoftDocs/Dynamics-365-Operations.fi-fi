---
title: Myyntiprovisioiden rekisteröinti
description: Tässä ohjeaiheessa kerrotaan, miten myyntiprovisiot lasketaan ja kirjataan.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c6dbccc3e2c33c8dfec2373bd21c7bd217a889b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203225"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="76ca0-103">Myyntiprovisioiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="76ca0-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76ca0-104">Tässä ohjeaiheessa kerrotaan, miten myyntiprovisiot lasketaan ja kirjataan.</span><span class="sxs-lookup"><span data-stu-id="76ca0-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="76ca0-105">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="76ca0-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="76ca0-106">Suorita ennen tämän opastuksen aloittamista Määritä myyntikomission säännöt -opastus ja varmista, että sinulla on kaikki tarvittavat komissiolaskelma-asetukset.</span><span class="sxs-lookup"><span data-stu-id="76ca0-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="76ca0-107">Kirjaa muistiin asiakasnumerot ja nimiketunnukset, jotka olevat valinnut provisioprosessiin, ja luo niillä pyydettäessä myyntitilaus tässä opastuksessa.</span><span class="sxs-lookup"><span data-stu-id="76ca0-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="76ca0-108">Laskuta myyntitilaus, josta myyjä saa provision</span><span class="sxs-lookup"><span data-stu-id="76ca0-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="76ca0-109">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="76ca0-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-110">Select **New**.</span></span>
3. <span data-ttu-id="76ca0-111">Valitse **Asiakastili**-kentässä avattavasta valikosta haluamasi tietue.</span><span class="sxs-lookup"><span data-stu-id="76ca0-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="76ca0-112">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-112">Select **OK**.</span></span>
5. <span data-ttu-id="76ca0-113">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="76ca0-114">Valitse **Vaihda näyttö**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-114">Select **Change view**.</span></span>
7. <span data-ttu-id="76ca0-115">Valitse **Otsikkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-115">Select **Header view**.</span></span>
8. <span data-ttu-id="76ca0-116">Laajenna osa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="76ca0-117">**Myyntiryhmä**-kentän arvo vastaa ryhmää, johon on määritetty vähintään yksi myyntiedustaja.</span><span class="sxs-lookup"><span data-stu-id="76ca0-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="76ca0-118">Ryhmän jäsenet saavat provisiot ennalta määritettyjen prosenttien ja jaon mukaisesti, kun tilaus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="76ca0-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="76ca0-119">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="76ca0-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="76ca0-120">Myös myyntiryhmä kopioidaan myyntitilausriville.</span><span class="sxs-lookup"><span data-stu-id="76ca0-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="76ca0-121">Voit muuttaa sitä niin, että se poikkeaa otsikon ja/tai rivien välisestä ryhmästä.</span><span class="sxs-lookup"><span data-stu-id="76ca0-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="76ca0-122">**Provisioryhmä**-kentän arvo vastaa ryhmää, jonka olet luonut vähintään yhdelle asiakkaalle provisioiden seurantaa varten.</span><span class="sxs-lookup"><span data-stu-id="76ca0-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="76ca0-123">Arvo kopioidaan asiakaskortista, mutta voit vaihtaa sen halutessasi.</span><span class="sxs-lookup"><span data-stu-id="76ca0-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="76ca0-124">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="76ca0-125">Valitse **Vaihda näyttö**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-125">Select **Change view**.</span></span>
11. <span data-ttu-id="76ca0-126">Valitse **Rivinäkymä**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-126">Select **Line view**.</span></span>
12. <span data-ttu-id="76ca0-127">Valitse **Nimiketunnus**-kentän pudotusvalikosta nimike, jonka olet määrittänyt provisioille.</span><span class="sxs-lookup"><span data-stu-id="76ca0-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="76ca0-128">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="76ca0-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="76ca0-129">Kirjoita rivin nettosumma muistiin.</span><span class="sxs-lookup"><span data-stu-id="76ca0-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="76ca0-130">Se vastaa myyntituottoa, joka on tässä esimerkissä provisiolaskelman peruste.</span><span class="sxs-lookup"><span data-stu-id="76ca0-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="76ca0-131">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-131">Select **Save**.</span></span>
15. <span data-ttu-id="76ca0-132">Valitse toimintoruudussa **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="76ca0-133">Valitse **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="76ca0-134">Laajenna **Parametrit**-osa.</span><span class="sxs-lookup"><span data-stu-id="76ca0-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="76ca0-135">Valitse **Määrä**-kentässä **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="76ca0-136">Valitse **Kirjaus**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="76ca0-137">Valitse **OK**ja valitse sitten seuraavassa ruudussa **OK**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="76ca0-138">Tapahtuman kirjaaminen kestää noin minuutin.</span><span class="sxs-lookup"><span data-stu-id="76ca0-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="76ca0-139">Anna käsittelyn valmistua äläkä sulje sivua.</span><span class="sxs-lookup"><span data-stu-id="76ca0-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="76ca0-140">Tarkastele rekisteröityjä myyntiprovisioita</span><span class="sxs-lookup"><span data-stu-id="76ca0-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="76ca0-141">Valitse toimintoruudussa **Lasku**, ja valitse sitten jälleen **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="76ca0-142">Valitse toimintoruudussa **Lasku**, ja valitse sitten **Provisiotapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="76ca0-143">**Yhteenveto**-välilehti sisältää rivit, jotka vastaavat laskutettuun myyntitilaukseen liitetyille myyntiedustajille maksettavia provisiosummia.</span><span class="sxs-lookup"><span data-stu-id="76ca0-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="76ca0-144">Tarkastellaan tietoja tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="76ca0-144">Let's review the details.</span></span>  
    - <span data-ttu-id="76ca0-145">Jos määritit **Provisiomyynti**-ryhmän Määritä myyntiprovision säännöt -opastuksessa, kaksi myyjää saa myyntiprovisioita ja provisio jaetaan tasan heidän keskeen.</span><span class="sxs-lookup"><span data-stu-id="76ca0-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="76ca0-146">Tässä esimerkissä provision kokonaismäärä lasketaan myyntituoton prosenttiosuutena (tilausrivin nettosumma).</span><span class="sxs-lookup"><span data-stu-id="76ca0-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="76ca0-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="76ca0-147">Close the page.</span></span>
4. <span data-ttu-id="76ca0-148">Valitse **Tosite**.</span><span class="sxs-lookup"><span data-stu-id="76ca0-148">Select **Voucher**.</span></span> <span data-ttu-id="76ca0-149">Voit tarkastella esimääritetyille provision kulu- ja ostoreskontratileille kirjattujen provisiosummien tositetapahtumia.</span><span class="sxs-lookup"><span data-stu-id="76ca0-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

