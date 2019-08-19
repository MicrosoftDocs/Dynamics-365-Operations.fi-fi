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
ms.openlocfilehash: 00ce4a31c0b0f466911658c79f6e32788273c127
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833999"
---
# <a name="manage-order-holds"></a><span data-ttu-id="1e767-103">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="1e767-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e767-104">Tämä menettely näyttää, miten asiakkaan myyntitilaukset asetetaan pitoon, miten tilauksen pitojen uloskuittausten kanssa toimitaan ja miten tilauksen pito poistetaan.</span><span class="sxs-lookup"><span data-stu-id="1e767-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="1e767-105">Tilaus on saatettu asettaa pitoon monesta eri syystä.</span><span class="sxs-lookup"><span data-stu-id="1e767-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="1e767-106">Voit esimerkiksi pitää tilausta, kunnes asiakkaan osoite tai maksutapa voidaan varmistaa tai kunnes johtaja voi tarkistaa asiakkaan luottorajan.</span><span class="sxs-lookup"><span data-stu-id="1e767-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="1e767-107">Varasto ei voi käsitellä pidossa olevaa tilausta toimitusta varten.</span><span class="sxs-lookup"><span data-stu-id="1e767-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="1e767-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="1e767-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="1e767-109">Tilauksen pitojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1e767-109">Set up order holds</span></span>
1. <span data-ttu-id="1e767-110">Valitse Myynti ja markkinointi > Asetukset > Myyntitilaukset > Tilauksen pitokoodit.</span><span class="sxs-lookup"><span data-stu-id="1e767-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="1e767-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1e767-111">Click New.</span></span>
3. <span data-ttu-id="1e767-112">Kirjoita arvo Pitokoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1e767-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="1e767-113">Kirjoita esimerkiksi Uusintapuhelu.</span><span class="sxs-lookup"><span data-stu-id="1e767-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="1e767-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1e767-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1e767-115">Esimerkki: Tilaus odottaa asiakkaan uusintapuhelua.</span><span class="sxs-lookup"><span data-stu-id="1e767-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="1e767-116">Voit halutessasi poistaa fyysiset varaukset tilauksesta valitsemalla Poistetut varaukset -valintaruudun, kun tämä pitokoodi lisätään.</span><span class="sxs-lookup"><span data-stu-id="1e767-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="1e767-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1e767-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="1e767-118">Tilauksen asettaminen pitoon</span><span class="sxs-lookup"><span data-stu-id="1e767-118">Place order on hold</span></span>
1. <span data-ttu-id="1e767-119">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1e767-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="1e767-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1e767-120">Click New.</span></span>
3. <span data-ttu-id="1e767-121">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1e767-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="1e767-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1e767-122">Click OK.</span></span>
5. <span data-ttu-id="1e767-123">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1e767-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="1e767-124">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1e767-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="1e767-125">Valitse toimintoruudussa Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1e767-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="1e767-126">Valitse Tilausten pidot.</span><span class="sxs-lookup"><span data-stu-id="1e767-126">Click Order holds.</span></span>
9. <span data-ttu-id="1e767-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1e767-127">Click New.</span></span>
10. <span data-ttu-id="1e767-128">Valitse Pitokoodi-kentässä edellisessä alitehtävässä luotu koodi.</span><span class="sxs-lookup"><span data-stu-id="1e767-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="1e767-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1e767-129">Click Save.</span></span>
12. <span data-ttu-id="1e767-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1e767-130">Close the page.</span></span>
13. <span data-ttu-id="1e767-131">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="1e767-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="1e767-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1e767-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1e767-133">Tällä hetkellä pidossa olevien tilausten Älä käsittele- ja Pito-kentät on merkitty.</span><span class="sxs-lookup"><span data-stu-id="1e767-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="1e767-134">Valitse toimintoruudussa Kerää ja pakkaa.</span><span class="sxs-lookup"><span data-stu-id="1e767-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="1e767-135">Tilausten pidon hallinta</span><span class="sxs-lookup"><span data-stu-id="1e767-135">Manage order holds</span></span>
1. <span data-ttu-id="1e767-136">Valitse Myynti ja markkinointi > Myyntitilaukset > Avoimet tilaukset > Tilausten pidot.</span><span class="sxs-lookup"><span data-stu-id="1e767-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="1e767-137">Tilausten pidot -sivu on kuin eräänlainen työtila, jossa on yhteenveto kaikista nykyisistä ja käsitellyistä pidoista ja jossa voit käsitellä niitä ja liitettyjä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="1e767-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="1e767-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1e767-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="1e767-139">Valitse toimintoruudussa Pidä uloskuittaus.</span><span class="sxs-lookup"><span data-stu-id="1e767-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="1e767-140">Valitse Kuittaa ulos.</span><span class="sxs-lookup"><span data-stu-id="1e767-140">Click Check out.</span></span>
5. <span data-ttu-id="1e767-141">Poista valitun rivin merkintä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1e767-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="1e767-142">Käyttäjätunnuksesi näkyy nyt uloskuittauksen kentässä.</span><span class="sxs-lookup"><span data-stu-id="1e767-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="1e767-143">Valitse Poista uloskuittaus.</span><span class="sxs-lookup"><span data-stu-id="1e767-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="1e767-144">Valitse toimintoruudussa Vapauta pito.</span><span class="sxs-lookup"><span data-stu-id="1e767-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="1e767-145">Kun olet valmis poistamaan pidon ja sallimaan tilauksen käsittelyn tilauksen täyttämisen seuraavaan vaiheeseen, pito on vapautettava.</span><span class="sxs-lookup"><span data-stu-id="1e767-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="1e767-146">Voit tilausta ei tarvitse muuttaa, voi suorittaa Vapauta pidot -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="1e767-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="1e767-147">Käytä kuitenkin Vapauta ja muokkaa -toimintoa, jos tilaus on päivitettävä vapautuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1e767-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="1e767-148">Vapauta ja lähetä -toiminto on käytettävissä vain, kun käytät Puhelinkeskus-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="1e767-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="1e767-149">Valitse Vapauta pidot.</span><span class="sxs-lookup"><span data-stu-id="1e767-149">Click Clear holds.</span></span>
    * <span data-ttu-id="1e767-150">Tilauksen pito on nyt vapautettu ja se on poistettu aktiivisten pitojen luettelosta.</span><span class="sxs-lookup"><span data-stu-id="1e767-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="1e767-151">Jos haluat nähdä kaikki pidot tai niiden alijoukot tietyn tilaan mukaan, muuta Näytä-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="1e767-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

