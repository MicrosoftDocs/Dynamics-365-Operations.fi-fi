---
title: Ostotilauksen tuotteiden vastaanoton kirjaaminen
description: Tässä aiheessa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.
author: FrankDahl
manager: AnnBe
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31690d58d32a93d4cba873e951c26856d3f9cc09
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147316"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="af9ed-103">Ostotilauksen tuotteiden vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="af9ed-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af9ed-104">Tässä aiheessa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="af9ed-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="af9ed-105">On myös mahdollista rekisteröidä tuotteiden vastaanotto varastoon ja kirjata ne myöhemmin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="af9ed-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="af9ed-106">Tämän tehtävän suorittaa yleensä ostoedustaja tai ostoreskontran koordinaattori.</span><span class="sxs-lookup"><span data-stu-id="af9ed-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="af9ed-107">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="af9ed-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="af9ed-108">Esimerkki sisältää yksinkertaisen ostotilauksen luomisvaiheet siten, että voit toistaa menettelyn tehtäväoppaana.</span><span class="sxs-lookup"><span data-stu-id="af9ed-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="af9ed-109">Jos käytät menettelyä omilla tiedoilla, aloita **Tavaran vastaanoton kirjaaminen** -alitehtävästä.</span><span class="sxs-lookup"><span data-stu-id="af9ed-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="af9ed-110">Valmistele uusi ostotilaus tavaroiden vastaanottoa varten</span><span class="sxs-lookup"><span data-stu-id="af9ed-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="af9ed-111">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="af9ed-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-112">Select **New**.</span></span>
3. <span data-ttu-id="af9ed-113">Kirjoita **Toimittajan tili** -kenttään arvoksi `US-101`.</span><span class="sxs-lookup"><span data-stu-id="af9ed-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="af9ed-114">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-114">Select **OK**.</span></span>
5. <span data-ttu-id="af9ed-115">Kirjoita **Nimiketunnus**-kenttään arvo `M0001`.</span><span class="sxs-lookup"><span data-stu-id="af9ed-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="af9ed-116">Kirjoita **Määrä**-kenttään `5`.</span><span class="sxs-lookup"><span data-stu-id="af9ed-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="af9ed-117">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="af9ed-118">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="af9ed-119">Tavaran vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="af9ed-119">Record receipt of goods</span></span>
1. <span data-ttu-id="af9ed-120">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="af9ed-121">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-121">Select **Product receipt**.</span></span> <span data-ttu-id="af9ed-122">**Määrä**-kentän avulla voit valita haluamasi vastaanotettavan määrän.</span><span class="sxs-lookup"><span data-stu-id="af9ed-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="af9ed-123">Jos määrä on esimerkiksi jo rekisteröity varastossa, voit valita **Rekisteröity määrä**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="af9ed-124">Tässä esimerkissä käytetään arvoa **Tilattu määrä**</span><span class="sxs-lookup"><span data-stu-id="af9ed-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="af9ed-125">Laajenna **Yleiskatsaus**-osa.</span><span class="sxs-lookup"><span data-stu-id="af9ed-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="af9ed-126">Kirjoita mikä tahansa arvo **Tuotteen vastaanotto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="af9ed-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="af9ed-127">Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="af9ed-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="af9ed-128">Laajenna **Rivit**-osa.</span><span class="sxs-lookup"><span data-stu-id="af9ed-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="af9ed-129">Valitse **määräksi** 4.</span><span class="sxs-lookup"><span data-stu-id="af9ed-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="af9ed-130">Tähän pystyt määrittämään manuaalisesti vastaanotettavan määrän kullekin tilauksen riville.</span><span class="sxs-lookup"><span data-stu-id="af9ed-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="af9ed-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="af9ed-131">Select **OK**.</span></span> <span data-ttu-id="af9ed-132">Tavarat nyt tallennettuja vastaanotetuiksi ostotilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansioasiakirja on luotu.</span><span class="sxs-lookup"><span data-stu-id="af9ed-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="af9ed-133">Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu ja milloin.</span><span class="sxs-lookup"><span data-stu-id="af9ed-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

