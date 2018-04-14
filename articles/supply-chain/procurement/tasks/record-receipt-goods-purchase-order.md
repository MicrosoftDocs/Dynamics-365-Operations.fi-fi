--- 
title: Ostotilauksen tuotteiden vastaanoton kirjaaminen
description: "Seuraavassa menettelyssä kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d8a47dac61705831b330f7b4939a18c865a8ace7
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="048a7-103">Ostotilauksen tuotteiden vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="048a7-103">Record the receipt of goods on the purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="048a7-104">Seuraavassa menettelyssä kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="048a7-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="048a7-105">On myös mahdollista rekisteröidä tuotteiden vastaanotto varastoon ja kirjata ne myöhemmin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="048a7-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="048a7-106">Tämän tehtävän suorittaa yleensä ostoedustaja tai ostoreskontran koordinaattori.</span><span class="sxs-lookup"><span data-stu-id="048a7-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="048a7-107">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="048a7-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="048a7-108">Esimerkki sisältää yksinkertaisen ostotilauksen luomisvaiheet siten, että voit toistaa menettelyn tehtäväoppaana.</span><span class="sxs-lookup"><span data-stu-id="048a7-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="048a7-109">Jos käytät menettelyä omilla tiedoilla, aloita Tavaran vastaanoton kirjaaminen -alitehtävästä.</span><span class="sxs-lookup"><span data-stu-id="048a7-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="048a7-110">Valmistele uusi ostotilaus tavaroiden vastaanottoa varten</span><span class="sxs-lookup"><span data-stu-id="048a7-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="048a7-111">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="048a7-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="048a7-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="048a7-112">Click New.</span></span>
3. <span data-ttu-id="048a7-113">Kirjoita Toimittajan tili -kenttään arvoksi US-101.</span><span class="sxs-lookup"><span data-stu-id="048a7-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="048a7-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="048a7-114">Click OK.</span></span>
5. <span data-ttu-id="048a7-115">Kirjoita Nimiketunnus-kenttään arvo M0001.</span><span class="sxs-lookup"><span data-stu-id="048a7-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="048a7-116">Kirjoita 5 Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="048a7-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="048a7-117">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="048a7-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="048a7-118">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="048a7-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="048a7-119">Tavaran vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="048a7-119">Record receipt of goods</span></span>
1. <span data-ttu-id="048a7-120">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="048a7-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="048a7-121">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="048a7-121">Click Product receipt.</span></span>
    * <span data-ttu-id="048a7-122">Määrä-kentän avulla voit valita haluamasi vastaanotettavan määrän.</span><span class="sxs-lookup"><span data-stu-id="048a7-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="048a7-123">Jos määrä on esimerkiksi jo rekisteröity varastossa, voit valita rekisteröidyn määrän.</span><span class="sxs-lookup"><span data-stu-id="048a7-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="048a7-124">Tässä esimerkissä käytetään tilattua määrää.</span><span class="sxs-lookup"><span data-stu-id="048a7-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="048a7-125">Kirjoita mikä tahansa arvo Tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="048a7-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="048a7-126">Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="048a7-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="048a7-127">Laajenna Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="048a7-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="048a7-128">Valitse määräksi 4.</span><span class="sxs-lookup"><span data-stu-id="048a7-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="048a7-129">Tähän pystyt määrittämään manuaalisesti vastaanotettavan määrän kullekin tilauksen riville.</span><span class="sxs-lookup"><span data-stu-id="048a7-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="048a7-130">Tiivistä Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="048a7-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="048a7-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="048a7-131">Click OK.</span></span>
    * <span data-ttu-id="048a7-132">Tavarat nyt tallennettuja vastaanotetuiksi ostotilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansioasiakirja on luotu.</span><span class="sxs-lookup"><span data-stu-id="048a7-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="048a7-133">Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu ja milloin.</span><span class="sxs-lookup"><span data-stu-id="048a7-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


