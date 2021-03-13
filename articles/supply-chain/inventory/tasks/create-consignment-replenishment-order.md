---
title: Luo tavaralähetyksen täydennystilaus
description: Tässä aiheessa kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon.
author: RichardLuan
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27b4d87add38fac29c9eba4ace08af91f9faca1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020151"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="aa138-103">Luo tavaralähetyksen täydennystilaus</span><span class="sxs-lookup"><span data-stu-id="aa138-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa138-104">Tässä aiheessa kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon.</span><span class="sxs-lookup"><span data-stu-id="aa138-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="aa138-105">Se siinä kuvataan myös, miten tuotteiden vastaanotto kirjataan niin, että tavaralähetysvarasto rekisteröidään käytettäväksi varastoksi, jonka omistaa toimittaja.</span><span class="sxs-lookup"><span data-stu-id="aa138-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="aa138-106">Tämä on yleensä hankinta-asiantuntijan tehtävä.</span><span class="sxs-lookup"><span data-stu-id="aa138-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="aa138-107">Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa.</span><span class="sxs-lookup"><span data-stu-id="aa138-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="aa138-108">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="aa138-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="aa138-109">Luo tavaralähetyksen täydennystilaus</span><span class="sxs-lookup"><span data-stu-id="aa138-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="aa138-110">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Tavaralähetys > Tavaralähetyksen täydennystilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aa138-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="aa138-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="aa138-111">Select **New**.</span></span>
3. <span data-ttu-id="aa138-112">Valitse **Toimittajatili**-kentässä toimittaja **US-104** (sinun on valittava toimittaja, joka on rekisteröity omistajaksi **varaston omistajat** -sivulla).</span><span class="sxs-lookup"><span data-stu-id="aa138-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="aa138-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa138-113">Select **OK**.</span></span>
5. <span data-ttu-id="aa138-114">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="aa138-114">Select **Add line**.</span></span>
6. <span data-ttu-id="aa138-115">Kirjoita **Nimiketunnus**-kenttään `M9211CI` (sinun on valittava nimike, joka on määritetty lähetysvarastoa varten).</span><span class="sxs-lookup"><span data-stu-id="aa138-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="aa138-116">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="aa138-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="aa138-117">Kirjoita päivämäärä **Pyydetty toimituspäivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa138-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="aa138-118">MRP-moduuli käyttää pyydettyä ja vahvistettua päivämäärää tavaroiden saapumisen arviointiin.</span><span class="sxs-lookup"><span data-stu-id="aa138-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="aa138-119">Kirjoita päivämäärä **Vahvistettu toimituspäivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa138-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="aa138-120">Laajenna **Rivin erittely** -osa.</span><span class="sxs-lookup"><span data-stu-id="aa138-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="aa138-121">Valitse **Varastodimensiot**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="aa138-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="aa138-122">Saat omistajan näkyviin **Varastodimensioiden omistaja** -kenttään päivittämällä sivun.</span><span class="sxs-lookup"><span data-stu-id="aa138-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="aa138-123">Toimittaja US-104 on nyt merkitty omistaja.</span><span class="sxs-lookup"><span data-stu-id="aa138-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="aa138-124">Tarkista varastotapahtuman tila</span><span class="sxs-lookup"><span data-stu-id="aa138-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="aa138-125">Valitse **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="aa138-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="aa138-126">Valitse **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="aa138-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="aa138-127">Huomaa halutulla rivillä, että **Vastaanotto**-kentän arvo on **Tilattu**.</span><span class="sxs-lookup"><span data-stu-id="aa138-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="aa138-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa138-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="aa138-129">Vastaanota nimikkeet</span><span class="sxs-lookup"><span data-stu-id="aa138-129">Receive items</span></span>
1. <span data-ttu-id="aa138-130">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="aa138-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="aa138-131">Kirjoita arvo **Ulkoisen tuotteen vastaanotto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa138-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="aa138-132">Syötä **Määrä**-kenttään numero, joka on pienempi kuin numero, joka siinä on.</span><span class="sxs-lookup"><span data-stu-id="aa138-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="aa138-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa138-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="aa138-134">Tarkista käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="aa138-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="aa138-135">Valitse **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="aa138-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="aa138-136">Valitse **Varastosaldo**.</span><span class="sxs-lookup"><span data-stu-id="aa138-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="aa138-137">Valitse **Yleiskatsaus**.</span><span class="sxs-lookup"><span data-stu-id="aa138-137">Select **Overview**.</span></span> <span data-ttu-id="aa138-138">Toimitusvarastoon vastaanotetut nimikkeet, jotka omistaa toimittaja ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="aa138-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="aa138-139">Tavaralähetyksen täydennystilauksella jäljellä oleva määrä näytetään **Tilattu yhteensä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="aa138-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="aa138-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="aa138-140">Close the page.</span></span>

