---
title: Ostotilauksen luominen myyntitilauksesta
description: Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843382"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="e0fdb-103">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="e0fdb-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0fdb-104">Tässä menettelyssä käsitellään, miten myyntitilaukseen perustuva ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="e0fdb-105">Ostotilauksen tuotteen määrät määritetään sitten täyttämään alkuperäisen ostotilauksen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="e0fdb-106">Myynnin kysynnän täyttäminen tällä tavoin on vaihtoehto kattavammalle ja optimoidulle jakelutarpeiden suunnittelumenetelmälle.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="e0fdb-107">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="e0fdb-108">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="e0fdb-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="e0fdb-109">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="e0fdb-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-110">Click New.</span></span>
3. <span data-ttu-id="e0fdb-111">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e0fdb-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e0fdb-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-113">Click OK.</span></span>
6. <span data-ttu-id="e0fdb-114">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e0fdb-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0fdb-116">Jos käytössä on USMF, voit valita D0001.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="e0fdb-117">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="e0fdb-118">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-118">Click Add line.</span></span>
10. <span data-ttu-id="e0fdb-119">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e0fdb-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0fdb-121">Jos käytössä on USMF, voit valita T0020.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="e0fdb-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e0fdb-123">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="e0fdb-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-124">Click Save.</span></span>
15. <span data-ttu-id="e0fdb-125">Valitse toimintoruudussa Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="e0fdb-126">Valitse Ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-126">Click Purchase order.</span></span>
    * <span data-ttu-id="e0fdb-127">Luo ostotilaus -sivulla on luettelo kaikista myyntitilauksesta kopioiduista avoimista myyntitilausriveistä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="e0fdb-128">Voit tarkastella tilauksen tietoja ja tarvittaessa muokata valittuja tietoja, kuten määrää ja hinnoitteluehtoja, ennen ostojen luontia.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="e0fdb-129">Valitse Sisällytä kaikki -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-129">Select the Include all option.</span></span>
    * <span data-ttu-id="e0fdb-130">Jos haluat muodostaa ostotilauksen vain myyntitilausrivien alijoukolle, valitse ne yksitellen.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="e0fdb-131">Toimittajatili-kenttään on ehkä jo lisätty toimittajanumero.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="e0fdb-132">Jos tuotteelle on määritetty oletustoimittaja (liitetyssä nimikekattavuudessa), kyseinen toimittaja kopioidaan riville.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="e0fdb-133">Muussa tapauksessa toimittaja on annettava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="e0fdb-134">Tämän opastuksen seuraavissa vaiheissa pyydetään valitsemaan uusi jokaiselle riville eri toimittaja. Näin toimitaan riippumatta siitä, onko Toimittajatili-kentässä arvo vai ei.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="e0fdb-135">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="e0fdb-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="e0fdb-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="e0fdb-138">Valitse toinen tilausrivi.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-138">Select the second order line.</span></span>
22. <span data-ttu-id="e0fdb-139">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="e0fdb-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="e0fdb-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="e0fdb-142">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-142">Click Validate.</span></span>
26. <span data-ttu-id="e0fdb-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-143">Click OK.</span></span>
    * <span data-ttu-id="e0fdb-144">Sanoma ilmoittaa, että vähintään yksi ostotilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="e0fdb-145">Järjestelmän muodostaa erillisen ostotilauksen kullekin myyntitilausriveille määritetylle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="e0fdb-146">Tämä tarkoittaa sitä, että jos sama toimittaja toimittaa useita myyntitilausrivejä, ostotilauksia luodaan yksi mutta siinä on useita rivejä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="e0fdb-147">Tarkastele myyntitilauksista luotuja ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="e0fdb-148">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="e0fdb-149">Valitse Liittyvät tilaukset.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-149">Click Related orders.</span></span>
    * <span data-ttu-id="e0fdb-150">Liittyvät tilaukset -sivulla on luettelo kaikista myyntitilauksesta luoduista tilauksista.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="e0fdb-151">Tässä esimerkissä on muodostettu kaksi ostotilausta kahdelle eri toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="e0fdb-152">Siirry eteenpäin napsauttamalla Ostotilaus-kentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="e0fdb-153">Jokainen ostotilausrivi on liitetty ostoon johtaneeseen myyntitilausriviin.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="e0fdb-154">Suhde myyntitilaukseen on ilmaistu Tuote-välilehden Rivin erittely -pikavälilehden Viitetyyppi-, Viitenumero- ja Viite-erä-kentissä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="e0fdb-155">Laajenna tai tiivistä Rivitiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="e0fdb-156">Valitse Tuote-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-156">Click the Product tab.</span></span>
    * <span data-ttu-id="e0fdb-157">Viite-erä varmistaa, että oston kustannukset veloitetaan siihen liitetyssä myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="e0fdb-158">Voit siirtyä alkuperäiseen myyntitilaukseen avaamalla linkin Viitenumero-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e0fdb-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

