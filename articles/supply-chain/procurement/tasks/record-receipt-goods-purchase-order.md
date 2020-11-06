---
title: Ostotilauksen tuotteiden vastaanoton kirjaaminen
description: Tässä aiheessa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd8ca2cbd24f326c4eaf9cd39e32de0eca81149d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018603"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="53d18-103">Ostotilauksen tuotteiden vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="53d18-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53d18-104">Tässä aiheessa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="53d18-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="53d18-105">On myös mahdollista rekisteröidä tuotteiden vastaanotto varastoon ja kirjata ne myöhemmin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="53d18-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="53d18-106">Tämän tehtävän suorittaa yleensä ostoedustaja tai ostoreskontran koordinaattori.</span><span class="sxs-lookup"><span data-stu-id="53d18-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="53d18-107">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="53d18-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="53d18-108">Esimerkki sisältää yksinkertaisen ostotilauksen luomisvaiheet siten, että voit toistaa menettelyn tehtäväoppaana.</span><span class="sxs-lookup"><span data-stu-id="53d18-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="53d18-109">Jos käytät menettelyä omilla tiedoilla, aloita **Tavaran vastaanoton kirjaaminen** -alitehtävästä.</span><span class="sxs-lookup"><span data-stu-id="53d18-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="53d18-110">Valmistele uusi ostotilaus tavaroiden vastaanottoa varten</span><span class="sxs-lookup"><span data-stu-id="53d18-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="53d18-111">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="53d18-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="53d18-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="53d18-112">Select **New**.</span></span>
3. <span data-ttu-id="53d18-113">Kirjoita **Toimittajan tili** -kenttään arvoksi `US-101`.</span><span class="sxs-lookup"><span data-stu-id="53d18-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="53d18-114">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d18-114">Select **OK**.</span></span>
5. <span data-ttu-id="53d18-115">Kirjoita **Nimiketunnus** -kenttään arvo `M0001`.</span><span class="sxs-lookup"><span data-stu-id="53d18-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="53d18-116">Kirjoita **Määrä** -kenttään `5`.</span><span class="sxs-lookup"><span data-stu-id="53d18-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="53d18-117">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="53d18-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="53d18-118">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="53d18-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="53d18-119">Tavaran vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="53d18-119">Record receipt of goods</span></span>
1. <span data-ttu-id="53d18-120">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="53d18-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="53d18-121">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="53d18-121">Select **Product receipt**.</span></span> <span data-ttu-id="53d18-122">**Määrä** -kentän avulla voit valita haluamasi vastaanotettavan määrän.</span><span class="sxs-lookup"><span data-stu-id="53d18-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="53d18-123">Jos määrä on esimerkiksi jo rekisteröity varastossa, voit valita **Rekisteröity määrä**.</span><span class="sxs-lookup"><span data-stu-id="53d18-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="53d18-124">Tässä esimerkissä käytetään arvoa **Tilattu määrä**</span><span class="sxs-lookup"><span data-stu-id="53d18-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="53d18-125">Laajenna **Yleiskatsaus** -osa.</span><span class="sxs-lookup"><span data-stu-id="53d18-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="53d18-126">Kirjoita mikä tahansa arvo **Tuotteen vastaanotto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="53d18-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="53d18-127">Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.</span><span class="sxs-lookup"><span data-stu-id="53d18-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="53d18-128">Laajenna **Rivit** -osa.</span><span class="sxs-lookup"><span data-stu-id="53d18-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="53d18-129">Valitse **määräksi** 4.</span><span class="sxs-lookup"><span data-stu-id="53d18-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="53d18-130">Tähän pystyt määrittämään manuaalisesti vastaanotettavan määrän kullekin tilauksen riville.</span><span class="sxs-lookup"><span data-stu-id="53d18-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="53d18-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d18-131">Select **OK**.</span></span> <span data-ttu-id="53d18-132">Tavarat nyt tallennettuja vastaanotetuiksi ostotilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansioasiakirja on luotu.</span><span class="sxs-lookup"><span data-stu-id="53d18-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="53d18-133">Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu ja milloin.</span><span class="sxs-lookup"><span data-stu-id="53d18-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

