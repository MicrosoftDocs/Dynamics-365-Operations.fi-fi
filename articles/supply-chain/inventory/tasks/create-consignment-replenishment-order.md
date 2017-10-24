---
title: "Luo tavaralähetyksen täydennystilaus"
description: "Tässä menettelyssä kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="4878f-103">Luo tavaralähetyksen täydennystilaus</span><span class="sxs-lookup"><span data-stu-id="4878f-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4878f-104">Tässä menettelyssä kuvataan, miten luot tavaralähetyksen täydennystilauksen, jossa voit seurata odotettua toimittajan lähetystä tavaralähetysvarastoon.</span><span class="sxs-lookup"><span data-stu-id="4878f-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="4878f-105">Se siinä kuvataan myös, miten tuotteiden vastaanotto kirjataan niin, että tavaralähetysvarasto rekisteröidään käytettäväksi varastoksi, jonka omistaa toimittaja.</span><span class="sxs-lookup"><span data-stu-id="4878f-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="4878f-106">Tämä on yleensä hankinta-asiantuntijan tehtävä.</span><span class="sxs-lookup"><span data-stu-id="4878f-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="4878f-107">Voit käyttää tätä opastusta USMF-yrityksen demotiedoissa.</span><span class="sxs-lookup"><span data-stu-id="4878f-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="4878f-108">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="4878f-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="4878f-109">Luo tavaralähetyksen täydennystilaus</span><span class="sxs-lookup"><span data-stu-id="4878f-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="4878f-110">Siirry kohtaan Hankinta > Tavaralähetys > Tavaralähetyksen täydennystilaukset.</span><span class="sxs-lookup"><span data-stu-id="4878f-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="4878f-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4878f-111">Click New.</span></span>
3. <span data-ttu-id="4878f-112">Kirjoita Toimittajan tili -kenttään toimittaja US-104.</span><span class="sxs-lookup"><span data-stu-id="4878f-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="4878f-113">Sinun on valittava toimittaja, joka on rekisteröity omistajaksi Varaston omistajat -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4878f-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="4878f-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4878f-114">Click OK.</span></span>
5. <span data-ttu-id="4878f-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="4878f-115">Click Add line.</span></span>
6. <span data-ttu-id="4878f-116">Kirjoita Nimiketunnus-kenttään M9211CI.</span><span class="sxs-lookup"><span data-stu-id="4878f-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="4878f-117">Valitse nimike, joka on asetettu tavaralähetysvarastoon.</span><span class="sxs-lookup"><span data-stu-id="4878f-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="4878f-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4878f-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="4878f-119">Kirjoita päivämäärä Pyydetty toimituspäivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4878f-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="4878f-120">MRP-moduuli käyttää pyydettyä ja vahvistettua päivämäärää tavaroiden saapumisen arviointiin.</span><span class="sxs-lookup"><span data-stu-id="4878f-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="4878f-121">Kirjoita päivämäärä Vahvistettu toimituspäivämäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4878f-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="4878f-122">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="4878f-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="4878f-123">Valitse Varastodimensiot-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4878f-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="4878f-124">Saat omistajan näkyviin Varastodimensioiden omistaja -kenttään päivittämällä sivun.</span><span class="sxs-lookup"><span data-stu-id="4878f-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="4878f-125">Toimittaja US-104 on nyt merkitty omistaja.</span><span class="sxs-lookup"><span data-stu-id="4878f-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="4878f-126">Tarkista varastotapahtuman tila</span><span class="sxs-lookup"><span data-stu-id="4878f-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="4878f-127">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="4878f-127">Click Inventory.</span></span>
2. <span data-ttu-id="4878f-128">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="4878f-128">Click Transactions.</span></span>
3. <span data-ttu-id="4878f-129">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4878f-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4878f-130">Huomaa, että Vastaanotto-kentän arvo on Tilattu.</span><span class="sxs-lookup"><span data-stu-id="4878f-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="4878f-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4878f-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="4878f-132">Vastaanota nimikkeet</span><span class="sxs-lookup"><span data-stu-id="4878f-132">Receive items</span></span>
1. <span data-ttu-id="4878f-133">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="4878f-133">Click Product receipt.</span></span>
2. <span data-ttu-id="4878f-134">Kirjoita arvo Ulkoisen tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4878f-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="4878f-135">Syötä Määrä-kenttään numero, joka on pienempi kuin numero, joka siinä on.</span><span class="sxs-lookup"><span data-stu-id="4878f-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="4878f-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4878f-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="4878f-137">Tarkista käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="4878f-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="4878f-138">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="4878f-138">Click Inventory.</span></span>
2. <span data-ttu-id="4878f-139">Valitse Käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4878f-139">Click On-hand.</span></span>
3. <span data-ttu-id="4878f-140">Valitse Yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="4878f-140">Click Overview.</span></span>
    * <span data-ttu-id="4878f-141">Toimitusvarastoon vastaanotetut nimikkeet, jotka omistaa toimittaja ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4878f-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="4878f-142">Tavaralähetyksen täydennystilauksella jäljellä oleva määrä näytetään Tilattu yhteensä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4878f-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="4878f-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4878f-143">Close the page.</span></span>
5. <span data-ttu-id="4878f-144">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="4878f-144">Click Close.</span></span>

