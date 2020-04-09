---
title: Tilausten pidon hallinta
description: Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16e11be633cdffbc8ee3e206eb42e7e1a2f72b9c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146442"
---
# <a name="manage-order-holds"></a><span data-ttu-id="0ca4f-103">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="0ca4f-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ca4f-104">Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="0ca4f-105">Tilaus on saatettu asettaa pitoon monesta eri syystä.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="0ca4f-106">Voit esimerkiksi pitää tilausta, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa tai kunnes johtaja voi tarkistaa asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="0ca4f-107">Varasto ei voi käsitellä pidossa olevaa tilausta toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="0ca4f-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="0ca4f-109">Tilauksen pitojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0ca4f-109">Set up order holds</span></span>
1. <span data-ttu-id="0ca4f-110">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asetukset > Myyntitilaukset > Tilauksen pitokoodit**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="0ca4f-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-111">Click **New**.</span></span>
3. <span data-ttu-id="0ca4f-112">Kirjoita arvo **Pitokoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="0ca4f-113">Kirjoita esimerkiksi Uusintapuhelu.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="0ca4f-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="0ca4f-115">Esimerkki: Tilaus odottaa asiakkaan uusintapuhelua.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="0ca4f-116">Voit halutessasi poistaa fyysiset varaukset tilauksesta valitsemalla **Poista varaukset** -valintaruudun, kun tämä pitokoodi lisätään.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="0ca4f-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="0ca4f-118">Tilauksen asettaminen pitoon</span><span class="sxs-lookup"><span data-stu-id="0ca4f-118">Place order on hold</span></span>
1. <span data-ttu-id="0ca4f-119">Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="0ca4f-120">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-120">Click **New**.</span></span>
3. <span data-ttu-id="0ca4f-121">Syötä tai valitse arvo **Asiakastili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="0ca4f-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-122">Click **OK**.</span></span>
5. <span data-ttu-id="0ca4f-123">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="0ca4f-124">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="0ca4f-125">Valitse **toimintoruudussa** **Myyntitilaus**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="0ca4f-126">Valitse **Tilausten pidot**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="0ca4f-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-127">Click **New**.</span></span>
10. <span data-ttu-id="0ca4f-128">Valitse **Pitokoodi**-kentässä edellisessä alitehtävässä luotu koodi.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="0ca4f-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-129">Click **Save**.</span></span>
12. <span data-ttu-id="0ca4f-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-130">Close the page.</span></span>
13. <span data-ttu-id="0ca4f-131">Siirry kohtaan **Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="0ca4f-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-132">In the list, mark the selected row.</span></span> <span data-ttu-id="0ca4f-133">Tällä hetkellä pidossa olevien tilausten Älä käsittele- ja Pito-kentät on merkitty.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="0ca4f-134">Valitse toimintoruudussa **Kerää ja pakkaa**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="0ca4f-135">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="0ca4f-135">Manage order holds</span></span>
1. <span data-ttu-id="0ca4f-136">Valitse **Myynti ja markkinointi > Myyntitilaukset > Avoimet tilaukset > Tilausten pidot**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="0ca4f-137">**Tilausten pidot** -sivu on kuin eräänlainen työtila, jossa on yhteenveto kaikista nykyisistä ja käsitellyistä pidoista ja jossa voit käsitellä niitä ja liitettyjä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="0ca4f-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0ca4f-139">Valitse **toimintoruudussa** **Pidä uloskuittaus**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="0ca4f-140">Valitse **Kuittaa ulos**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-140">Click **Check out**.</span></span>
5. <span data-ttu-id="0ca4f-141">Poista valitun rivin merkintä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="0ca4f-142">Käyttäjätunnuksesi näkyy nyt **Uloskuittaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="0ca4f-143">Valitse **Poista uloskuittaus**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="0ca4f-144">Valitse **toimintoruudussa** **Vapauta pito**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="0ca4f-145">Kun olet valmis poistamaan pidon ja sallimaan tilauksen käsittelyn tilauksen täyttämisen seuraavaan vaiheeseen, pito on vapautettava.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="0ca4f-146">Voit tilausta ei tarvitse muuttaa, voi suorittaa Vapauta pidot -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="0ca4f-147">Käytä kuitenkin Vapauta ja muokkaa -toimintoa, jos tilaus on päivitettävä vapautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="0ca4f-148">**Vapauta ja lähetä** -toiminto on käytettävissä vain, kun käytät Puhelinkeskus-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="0ca4f-149">Valitse **Vapauta pidot**.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-149">Click **Clear holds**.</span></span> <span data-ttu-id="0ca4f-150">Tilauksen pito on nyt vapautettu ja se on poistettu aktiivisten pitojen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="0ca4f-151">Jos haluat nähdä kaikki pidot tai niiden alijoukot tietyn tilaan mukaan, muuta Näytä-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="0ca4f-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

