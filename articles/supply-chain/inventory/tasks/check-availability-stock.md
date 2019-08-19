---
title: Varastosaatavuuden tarkistus
description: Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b78b2e4ec3179450d635857353846c9bcb23eed
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795169"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="ffedb-103">Varastosaatavuuden tarkistus</span><span class="sxs-lookup"><span data-stu-id="ffedb-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffedb-104">Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="ffedb-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="ffedb-105">Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan.</span><span class="sxs-lookup"><span data-stu-id="ffedb-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="ffedb-106">Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa.</span><span class="sxs-lookup"><span data-stu-id="ffedb-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="ffedb-107">Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="ffedb-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="ffedb-108">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="ffedb-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="ffedb-109">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="ffedb-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="ffedb-110">Varastotyöntekijä tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="ffedb-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="ffedb-111">Nimikkeen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ffedb-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="ffedb-112">Valitse Inventoinnin- ja varastonhallinta > Kyselyt ja raportit > Käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="ffedb-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="ffedb-113">Valitse nimiketunnuksen rivi.</span><span class="sxs-lookup"><span data-stu-id="ffedb-113">Select the Item number row.</span></span>
    * <span data-ttu-id="ffedb-114">Voit tehdä kyselyn käytettävissä olevasta varastosta nimiketunnuksen perusteella valitsemalla rivin, jossa taulun arvoksi on määritetty Käytettävissä oleva varasto ja kentän arvoksi on määritetty Nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="ffedb-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="ffedb-115">Valitse Ehdot-kentässä nimike, josta haluat tehdä kyselyn.</span><span class="sxs-lookup"><span data-stu-id="ffedb-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="ffedb-116">Jos käytössä on esittely-yritys USMF:n tiedot, voit valita arvon M9201.</span><span class="sxs-lookup"><span data-stu-id="ffedb-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="ffedb-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ffedb-117">Click OK.</span></span>
5. <span data-ttu-id="ffedb-118">Valitse Dimensiot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-118">Click Dimensions.</span></span>
    * <span data-ttu-id="ffedb-119">Dimensiot-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="ffedb-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="ffedb-120">Jos tarvitset varaukseen liittyviä tietoja, kaikki varastonhallinnan prosessien lisätoimintoja käyttävien nimikkeiden varastodimensiot on näytettävä.</span><span class="sxs-lookup"><span data-stu-id="ffedb-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="ffedb-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ffedb-121">Click OK.</span></span>
7. <span data-ttu-id="ffedb-122">Valitse toimintoruudussa Liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="ffedb-123">Jos kohta ei ole näkyvissä, valitse ellipsipainike (…), jolloin näkyviin tulevat toimintoruudun lisävaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="ffedb-124">Valitse Toimituksen yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="ffedb-124">Click Supply overview.</span></span>
    * <span data-ttu-id="ffedb-125">Toimituksen yhteenveto -välilehdessä on tietyn nimikkeen tietoja, kuten käytettävissä oleva varasto, läpimenoaika ja toimittajan tiedot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="ffedb-126">Laajenna Varasto-osa.</span><span class="sxs-lookup"><span data-stu-id="ffedb-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="ffedb-127">Laajenna Toimittajat-osa.</span><span class="sxs-lookup"><span data-stu-id="ffedb-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="ffedb-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-128">Close the page.</span></span>
12. <span data-ttu-id="ffedb-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="ffedb-130">Fyysisen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="ffedb-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="ffedb-131">Valitse Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto.</span><span class="sxs-lookup"><span data-stu-id="ffedb-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="ffedb-132">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffedb-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ffedb-133">Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="ffedb-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="ffedb-134">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-134">Refresh the page.</span></span>
4. <span data-ttu-id="ffedb-135">Valitse Näytä dimensiot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="ffedb-136">Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="ffedb-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="ffedb-137">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ffedb-137">Click OK.</span></span>
6. <span data-ttu-id="ffedb-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="ffedb-139">Käytettävissä olevan varaston tarkistaminen sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="ffedb-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="ffedb-140">Valitse Varastonhallinta > Kyselyt ja raportit > Varastosaldon sijainnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="ffedb-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="ffedb-141">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ffedb-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="ffedb-142">Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.</span><span class="sxs-lookup"><span data-stu-id="ffedb-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="ffedb-143">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-143">Refresh the page.</span></span>
4. <span data-ttu-id="ffedb-144">Valitse Näytä dimensiot.</span><span class="sxs-lookup"><span data-stu-id="ffedb-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="ffedb-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ffedb-145">Click OK.</span></span>
6. <span data-ttu-id="ffedb-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ffedb-146">Close the page.</span></span>

