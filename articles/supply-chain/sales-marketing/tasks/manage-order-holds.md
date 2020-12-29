---
title: Tilausten pidon hallinta
description: Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9caf6651813f0111b873db1769140d973f1a2e3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427167"
---
# <a name="manage-order-holds"></a><span data-ttu-id="71b09-103">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="71b09-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71b09-104">Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.</span><span class="sxs-lookup"><span data-stu-id="71b09-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="71b09-105">Tilaus on saatettu asettaa pitoon monesta eri syystä.</span><span class="sxs-lookup"><span data-stu-id="71b09-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="71b09-106">Voit esimerkiksi pitää tilausta, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa tai kunnes johtaja voi tarkistaa asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="71b09-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="71b09-107">Varasto ei voi käsitellä pidossa olevaa tilausta toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="71b09-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="71b09-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="71b09-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="71b09-109">Tilauksen pitojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="71b09-109">Set up order holds</span></span>
1. <span data-ttu-id="71b09-110">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asetukset > Myyntitilaukset > Tilauksen pitokoodit**.</span><span class="sxs-lookup"><span data-stu-id="71b09-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="71b09-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="71b09-111">Click **New**.</span></span>
3. <span data-ttu-id="71b09-112">Kirjoita arvo **Pitokoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="71b09-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="71b09-113">Kirjoita esimerkiksi Uusintapuhelu.</span><span class="sxs-lookup"><span data-stu-id="71b09-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="71b09-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="71b09-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="71b09-115">Esimerkki: Tilaus odottaa asiakkaan uusintapuhelua.</span><span class="sxs-lookup"><span data-stu-id="71b09-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="71b09-116">Voit halutessasi poistaa fyysiset varaukset tilauksesta valitsemalla **Poista varaukset** -valintaruudun, kun tämä pitokoodi lisätään.</span><span class="sxs-lookup"><span data-stu-id="71b09-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="71b09-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="71b09-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="71b09-118">Tilauksen asettaminen pitoon</span><span class="sxs-lookup"><span data-stu-id="71b09-118">Place order on hold</span></span>
1. <span data-ttu-id="71b09-119">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="71b09-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="71b09-120">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="71b09-120">Click **New**.</span></span>
3. <span data-ttu-id="71b09-121">Syötä tai valitse arvo **Asiakastili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71b09-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="71b09-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="71b09-122">Click **OK**.</span></span>
5. <span data-ttu-id="71b09-123">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71b09-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="71b09-124">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="71b09-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="71b09-125">Valitse **toimintoruudussa** **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="71b09-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="71b09-126">Valitse **Tilausten pidot**.</span><span class="sxs-lookup"><span data-stu-id="71b09-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="71b09-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="71b09-127">Click **New**.</span></span>
10. <span data-ttu-id="71b09-128">Valitse **Pitokoodi**-kentässä edellisessä alitehtävässä luotu koodi.</span><span class="sxs-lookup"><span data-stu-id="71b09-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="71b09-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="71b09-129">Click **Save**.</span></span>
12. <span data-ttu-id="71b09-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="71b09-130">Close the page.</span></span>
13. <span data-ttu-id="71b09-131">Siirry kohtaan **Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="71b09-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="71b09-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="71b09-132">In the list, mark the selected row.</span></span> <span data-ttu-id="71b09-133">Tällä hetkellä pidossa olevien tilausten Älä käsittele- ja Pito-kentät on merkitty.</span><span class="sxs-lookup"><span data-stu-id="71b09-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="71b09-134">Valitse toimintoruudussa **Kerää ja pakkaa**.</span><span class="sxs-lookup"><span data-stu-id="71b09-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="71b09-135">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="71b09-135">Manage order holds</span></span>
1. <span data-ttu-id="71b09-136">Valitse **Myynti ja markkinointi > Myyntitilaukset > Avoimet tilaukset > Tilausten pidot**.</span><span class="sxs-lookup"><span data-stu-id="71b09-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="71b09-137">**Tilausten pidot** -sivu on kuin eräänlainen työtila, jossa on yhteenveto kaikista nykyisistä ja käsitellyistä pidoista ja jossa voit käsitellä niitä ja liitettyjä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="71b09-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="71b09-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="71b09-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="71b09-139">Valitse **toimintoruudussa** **Pidä uloskuittaus**.</span><span class="sxs-lookup"><span data-stu-id="71b09-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="71b09-140">Valitse **Kuittaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="71b09-140">Click **Check out**.</span></span>
5. <span data-ttu-id="71b09-141">Poista valitun rivin merkintä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="71b09-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="71b09-142">Käyttäjätunnuksesi näkyy nyt **Uloskuittaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="71b09-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="71b09-143">Valitse **Poista uloskuittaus**.</span><span class="sxs-lookup"><span data-stu-id="71b09-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="71b09-144">Valitse **toimintoruudussa** **Vapauta pito**.</span><span class="sxs-lookup"><span data-stu-id="71b09-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="71b09-145">Kun olet valmis poistamaan pidon ja sallimaan tilauksen käsittelyn tilauksen täyttämisen seuraavaan vaiheeseen, pito on vapautettava.</span><span class="sxs-lookup"><span data-stu-id="71b09-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="71b09-146">Voit tilausta ei tarvitse muuttaa, voi suorittaa Vapauta pidot -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="71b09-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="71b09-147">Käytä kuitenkin Vapauta ja muokkaa -toimintoa, jos tilaus on päivitettävä vapautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="71b09-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="71b09-148">**Vapauta ja lähetä** -toiminto on käytettävissä vain, kun käytät Puhelinkeskus-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="71b09-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="71b09-149">Valitse **Vapauta pidot**.</span><span class="sxs-lookup"><span data-stu-id="71b09-149">Click **Clear holds**.</span></span> <span data-ttu-id="71b09-150">Tilauksen pito on nyt vapautettu ja se on poistettu aktiivisten pitojen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="71b09-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="71b09-151">Jos haluat nähdä kaikki pidot tai niiden alijoukot tietyn tilaan mukaan, muuta Näytä-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="71b09-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

