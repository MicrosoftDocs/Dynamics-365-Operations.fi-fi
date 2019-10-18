---
title: Varastosaatavuuden tarkistus
description: Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2019
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
ms.openlocfilehash: e0c00b2a79ab588ff47c249f73570544d884b79e
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995241"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="7acab-103">Varastosaatavuuden tarkistus</span><span class="sxs-lookup"><span data-stu-id="7acab-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7acab-104">Tässä menettelyssä kerrotaan, miten tietyn nimiketunnuksen varastosaldo ja käytettävissä oleva varasto tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="7acab-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="7acab-105">Siinä näytetään myös, miten nimikkeeseen liittyvät toimitustiedot haetaan.</span><span class="sxs-lookup"><span data-stu-id="7acab-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="7acab-106">Fyysinen käytettävissä oleva varasto on käytettävissä oleva varastosaldo. Se tarkoittaa ostettua, vastaanotettua ja rekisteröityä varastoa.</span><span class="sxs-lookup"><span data-stu-id="7acab-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="7acab-107">Käytettävissä oleva varasto sisältää käytettävissä olevan varaston, mutta varaston, joka on tilattu ja jota odotetaan saapuvaksi, mutta jota ei ole vielä vastaanotettu tai rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="7acab-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="7acab-108">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="7acab-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="7acab-109">Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja.</span><span class="sxs-lookup"><span data-stu-id="7acab-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="7acab-110">Varastotyöntekijä tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7acab-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="7acab-111">Nimikkeen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="7acab-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="7acab-112">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="7acab-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="7acab-113">Valitse **Nimiketunnus**-rivi.</span><span class="sxs-lookup"><span data-stu-id="7acab-113">Select the **Item number** row.</span></span> <span data-ttu-id="7acab-114">Voit tehdä kyselyn käytettävissä olevasta varastosta nimiketunnuksen perusteella valitsemalla rivin, jossa taulun arvoksi on määritetty **Käytettävissä oleva varasto** ja kentän arvoksi on määritetty **Nimiketunnus**.</span><span class="sxs-lookup"><span data-stu-id="7acab-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="7acab-115">Valitse **Ehdot**-kentässä nimike, josta haluat tehdä kyselyn.</span><span class="sxs-lookup"><span data-stu-id="7acab-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="7acab-116">Jos käytössä on esittely-yritys USMF:n tiedot, voit valita arvon M9201.</span><span class="sxs-lookup"><span data-stu-id="7acab-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="7acab-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7acab-117">Click **OK**.</span></span>
5. <span data-ttu-id="7acab-118">Valitse **toimintoruudussa** **Dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="7acab-118">On the **Action pane**, click **Dimensions**.</span></span> <span data-ttu-id="7acab-119">**Dimensiot**-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="7acab-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="7acab-120">Jos tarvitset varaukseen liittyviä tietoja, kaikki varastonhallinnan prosessien lisätoimintoja käyttävien nimikkeiden varastodimensiot on näytettävä.</span><span class="sxs-lookup"><span data-stu-id="7acab-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>
6. <span data-ttu-id="7acab-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7acab-121">Click **OK**.</span></span>
7. <span data-ttu-id="7acab-122">Valitse **toimintoruudussa** **Liittyvät tiedot**.</span><span class="sxs-lookup"><span data-stu-id="7acab-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="7acab-123">Jos vaihtoehto ei ole näkyvissä, valitse kolme pistettä -painike (…), jolloin näkyviin tulevat toimintoruudun lisävaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="7acab-123">If you don’t see this option, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>
8. <span data-ttu-id="7acab-124">Valitse **Toimituksen yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="7acab-124">Click **Supply overview**.</span></span> <span data-ttu-id="7acab-125">**Toimituksen yhteenveto** -välilehdessä on tietyn nimikkeen tietoja, kuten käytettävissä oleva varasto, läpimenoaika ja toimittajan tiedot.</span><span class="sxs-lookup"><span data-stu-id="7acab-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="7acab-126">Laajenna **Varasto**-osa.</span><span class="sxs-lookup"><span data-stu-id="7acab-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="7acab-127">Laajenna **Toimittajat**-osa.</span><span class="sxs-lookup"><span data-stu-id="7acab-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="7acab-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-128">Close the page.</span></span>
12. <span data-ttu-id="7acab-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="7acab-130">Fyysisen käytettävissä olevan varaston tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="7acab-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="7acab-131">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Fyysinen käytettävissä oleva varasto**.</span><span class="sxs-lookup"><span data-stu-id="7acab-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="7acab-132">Kirjoita arvo **Nimiketunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7acab-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="7acab-133">Voit suodattaa nimikeluettelon Toimipaikka- ja Varasto-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="7acab-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="7acab-134">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-134">Refresh the page.</span></span>
4. <span data-ttu-id="7acab-135">Valitse **toimintoruudussa** **Näytä dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="7acab-135">On the **Action pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="7acab-136">Dimensionäyttö-välilehden avulla voit valita, miten tarkat tiedot haluat nähdä käytettävissä olevasta varastosta.</span><span class="sxs-lookup"><span data-stu-id="7acab-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="7acab-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7acab-137">Click **OK**.</span></span>
6. <span data-ttu-id="7acab-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="7acab-139">Käytettävissä olevan varaston tarkistaminen sijainnin mukaan</span><span class="sxs-lookup"><span data-stu-id="7acab-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="7acab-140">Valitse **Siirtymisruutu > Moduulit > Varastonhallinta > Kyselyt ja raportit > Varastosaldo sijainnin mukaan**.</span><span class="sxs-lookup"><span data-stu-id="7acab-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="7acab-141">Kirjoita arvo **Varasto**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7acab-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="7acab-142">Jos käytössä on esittelytietojen USMF-yritys, voit käyttää arvoa 51.</span><span class="sxs-lookup"><span data-stu-id="7acab-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="7acab-143">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-143">Refresh the page.</span></span>
4. <span data-ttu-id="7acab-144">Valitse **Näytä dimensiot**.</span><span class="sxs-lookup"><span data-stu-id="7acab-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="7acab-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7acab-145">Click **OK**.</span></span>
6. <span data-ttu-id="7acab-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7acab-146">Close the page.</span></span>

