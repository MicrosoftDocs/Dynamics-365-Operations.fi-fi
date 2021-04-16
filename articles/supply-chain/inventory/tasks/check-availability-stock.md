---
title: Varastosaatavuuden tarkistus
description: Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1b68a40ba433f7db6eb910961cd429629387bbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834094"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="9408a-103">Varastosaatavuuden tarkistus</span><span class="sxs-lookup"><span data-stu-id="9408a-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9408a-104">Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="9408a-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="9408a-105">Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan.</span><span class="sxs-lookup"><span data-stu-id="9408a-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="9408a-106">Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa.</span><span class="sxs-lookup"><span data-stu-id="9408a-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="9408a-107">Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="9408a-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="9408a-108">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="9408a-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="9408a-109">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="9408a-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="9408a-110">Varastotyöntekijä tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="9408a-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="9408a-111">Nimikkeen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="9408a-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="9408a-112">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="9408a-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="9408a-113">Valitse **Nimiketunnus**-rivi.</span><span class="sxs-lookup"><span data-stu-id="9408a-113">Select the **Item number** row.</span></span> <span data-ttu-id="9408a-114">Voit tehdä kyselyn käytettävissä olevasta varastosta nimiketunnuksen perusteella valitsemalla rivin, jossa taulun arvoksi on määritetty **Käytettävissä oleva varasto** ja kentän arvoksi on määritetty **Nimiketunnus**.</span><span class="sxs-lookup"><span data-stu-id="9408a-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="9408a-115">Valitse **Ehdot**-kentässä nimike, josta haluat tehdä kyselyn.</span><span class="sxs-lookup"><span data-stu-id="9408a-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="9408a-116">Jos käytössä on esittely-yritys USMF:n tiedot, voit valita arvon M9201.</span><span class="sxs-lookup"><span data-stu-id="9408a-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="9408a-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9408a-117">Click **OK**.</span></span>
5. <span data-ttu-id="9408a-118">Valitse **toimintoruudussa** **Dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9408a-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="9408a-119">**Dimensiot**-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="9408a-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="9408a-120">Jos tarvitset varaukseen liittyviä tietoja, kaikki varastonhallinnan prosessien lisätoimintoja käyttävien nimikkeiden varastodimensiot on näytettävä.</span><span class="sxs-lookup"><span data-stu-id="9408a-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="9408a-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9408a-121">Click **OK**.</span></span>
7. <span data-ttu-id="9408a-122">Valitse **toimintoruudussa** **Liittyvät tiedot**.</span><span class="sxs-lookup"><span data-stu-id="9408a-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="9408a-123">Jos vaihtoehto ei ole näkyvissä, valitse kolme pistettä -painike (…), jolloin näkyviin tulevat toimintoruudun lisävaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="9408a-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="9408a-124">Valitse **Toimituksen yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="9408a-124">Click **Supply overview**.</span></span> <span data-ttu-id="9408a-125">**Toimituksen yhteenveto** -välilehdessä on tietyn nimikkeen tietoja, kuten käytettävissä oleva varasto, läpimenoaika ja toimittajan tiedot.</span><span class="sxs-lookup"><span data-stu-id="9408a-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="9408a-126">Laajenna **Varasto**-osa.</span><span class="sxs-lookup"><span data-stu-id="9408a-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="9408a-127">Laajenna **Toimittajat**-osa.</span><span class="sxs-lookup"><span data-stu-id="9408a-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="9408a-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-128">Close the page.</span></span>
12. <span data-ttu-id="9408a-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="9408a-130">Fyysisen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="9408a-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="9408a-131">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="9408a-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="9408a-132">Kirjoita arvo **Nimiketunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9408a-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="9408a-133">Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="9408a-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="9408a-134">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-134">Refresh the page.</span></span>
4. <span data-ttu-id="9408a-135">Valitse **toimintoruudussa** **Näytä dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9408a-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="9408a-136">Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="9408a-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="9408a-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9408a-137">Click **OK**.</span></span>
6. <span data-ttu-id="9408a-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="9408a-139">Käytettävissä olevan varaston tarkistaminen sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="9408a-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="9408a-140">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Varastosaldo sijainnin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="9408a-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="9408a-141">Kirjoita arvo **Varasto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9408a-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="9408a-142">Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.</span><span class="sxs-lookup"><span data-stu-id="9408a-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="9408a-143">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-143">Refresh the page.</span></span>
4. <span data-ttu-id="9408a-144">Valitse **Näytä dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="9408a-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="9408a-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9408a-145">Click **OK**.</span></span>
6. <span data-ttu-id="9408a-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9408a-146">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]