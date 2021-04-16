---
title: Jaksota tuotantotyöt prosessivalmistukseen
description: Näissä toimintaohjeissa käytetään maalituotteita esimerkkinä suunniteltujen tilausten sarjoittamisesta värin ja pakkauskoon prioriteettien mukaan.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 461893c355ac2ebf8124591f93d025cae49081fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810969"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="dc4c8-103">Jaksota tuotantotyöt prosessivalmistukseen</span><span class="sxs-lookup"><span data-stu-id="dc4c8-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc4c8-104">Näissä toimintaohjeissa käytetään maalituotteita esimerkkinä suunniteltujen tilausten sarjoittamisesta värin ja pakkauskoon prioriteettien mukaan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="dc4c8-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USPI.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="dc4c8-106">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="dc4c8-107">Suorita pääsuunnittelu USPI:lle</span><span class="sxs-lookup"><span data-stu-id="dc4c8-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="dc4c8-108">Valitse Pääsuunnittelu > Pääsuunnittelu > Suorita > Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="dc4c8-109">Avaa haku valitsemalla Pääsuunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dc4c8-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dc4c8-111">Valitse MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="dc4c8-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-112">Click OK.</span></span>
    * <span data-ttu-id="dc4c8-113">Tämä käynnistää pääsuunnittelun, mukaan lukien sarjoitusprosessin.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="dc4c8-114">Tämä prosessi voi kestää muutamia minuutteja.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="dc4c8-115">Näytä maalituotteiden suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="dc4c8-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="dc4c8-116">Valitse Pääsuunnittelu > Pääsuunnittelu > Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="dc4c8-117">Laajenna nimikkeen tietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="dc4c8-118">Laajenna aikataulutietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="dc4c8-119">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dc4c8-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc4c8-121">Valitse MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="dc4c8-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dc4c8-123">Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P300 mukaan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="dc4c8-124">Avaa lukitus selataksesi oikealle, josta näet tilaus- ja toimituspäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="dc4c8-125">Huomaa, että nimikkeiden tilauspäivämäärä on tänään, ja että suunniteltujen tilausten toimituspäivämääriä ei sarjoiteta tärkeysjärjestykseen värin ja pakkauskoon mukaan, kuten tuotenimessä sanotaan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="dc4c8-126">Vie osoitin nimiketunnuksen päälle nähdäksesi tuotteen nimi ja prioriteetti.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="dc4c8-127">Sarjoita suunnitellut maalitilaukset</span><span class="sxs-lookup"><span data-stu-id="dc4c8-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="dc4c8-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-128">Close the page.</span></span>
2. <span data-ttu-id="dc4c8-129">Valitse Pääsuunnittelu > Pääsuunnittelu > Sarjoitetut suunnitellut tilaukset</span><span class="sxs-lookup"><span data-stu-id="dc4c8-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="dc4c8-130">Laajenna nimikkeen tietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="dc4c8-131">Laajenna aikataulutietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="dc4c8-132">Huomautus: Tässä voit nähdä, että suunniteltujen tilausten aloituspäivämäärä/-aika on sarjoitettu värin ja pakkauskoon mukaan 28 päivän aikajaksossa.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="dc4c8-133">Nämä jaksot on määritetty Kampanja-kentän numeron mukaan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="dc4c8-134">Sarjoitettu suunniteltu tilaus -lomake toimii samalla tavalla kuin tavallinen suunnitellun tilauksen lomake, ja tuotannon suunnittelija voi vahvistaa suunnitellut tilaukset täällä.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="dc4c8-135">Valitse kaikki rivit.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-135">Mark all rows.</span></span>
6. <span data-ttu-id="dc4c8-136">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-136">Click Accept.</span></span>
    * <span data-ttu-id="dc4c8-137">Tämä päivittää suunniteltuihin tilauksiin valitun sarjoitetun tehtävän, joka on joko Lykkää tai Aikaista.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="dc4c8-138">Vahvista suunniteltujen tilausten sarjoitus</span><span class="sxs-lookup"><span data-stu-id="dc4c8-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="dc4c8-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-139">Close the page.</span></span>
2. <span data-ttu-id="dc4c8-140">Valitse Pääsuunnittelu > Pääsuunnittelu > Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="dc4c8-141">Laajenna nimikkeen tietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="dc4c8-142">Laajenna aikataulutietojen tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="dc4c8-143">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dc4c8-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc4c8-145">Valitse MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="dc4c8-146">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dc4c8-147">Pikasuodattimen avulla voit suodattaa Nimiketunnus-kentän arvon P300 mukaan.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="dc4c8-148">Huomaa, että tilaukset nyt on sarjoitettu väri- ja kokoprioriteetin mukaan, ja suunnitellut tilaukset aloitetaan aikaisimpana tilaus- ja toimituspäivänä.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="dc4c8-149">Vahvista Tilauspäivämäärä-sarake tai Aloituspäivämäärä Ajoituksen tiedot -tietoruudussa.</span><span class="sxs-lookup"><span data-stu-id="dc4c8-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]