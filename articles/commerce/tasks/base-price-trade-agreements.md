---
title: Perushinta ja kauppasopimukset
description: Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412031"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="e5f0a-103">Perushinta ja kauppasopimukset</span><span class="sxs-lookup"><span data-stu-id="e5f0a-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5f0a-104">Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="e5f0a-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="e5f0a-106">Siirry **siirtymisruudussa** kohtaan **Moduulit > Retail ja Commerce > Hinnoittelun ja alennusten hallinta > Hintaryhmät > Kaikki hintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="e5f0a-107">Hintaryhmät tarkoittava tapaa, jolla kauppasopimukset on liitetty tiettyihin kanaviin.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="e5f0a-108">Jos hintaryhmiä käytetään kauppasopimusten liittämisessä kanaviin, käytössä on kanavakohtainen hinnoittelu.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="e5f0a-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-109">Click **New**.</span></span>
3. <span data-ttu-id="e5f0a-110">Syötä arvo **Hintaryhmät**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="e5f0a-111">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="e5f0a-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-112">Click **Save**.</span></span>
6. <span data-ttu-id="e5f0a-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-113">Close the page.</span></span>
7. <span data-ttu-id="e5f0a-114">Siirry **siirtymisruudussa** kohtaan **Moduulit > Retail ja Commerce > Kanavat > Myymälät > Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="e5f0a-115">Valitse luettelosta New York.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="e5f0a-116">Valitse toimintoruudussa **Myymälä**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="e5f0a-117">Valitse **Hintaryhmät**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="e5f0a-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-118">Click **New**.</span></span>
12. <span data-ttu-id="e5f0a-119">Avaa haku valitsemalla **Hintaryhmät**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="e5f0a-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e5f0a-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-121">Click **Save**.</span></span>
15. <span data-ttu-id="e5f0a-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-122">Close the page.</span></span>
16. <span data-ttu-id="e5f0a-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-123">Close the page.</span></span>
17. <span data-ttu-id="e5f0a-124">Siirry **siirtymisruudussa** kohtaan **Moduulit > Retail ja Commerce > Tuotteet ja luokat > Vapautetut tuotteet luokittain**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="e5f0a-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="e5f0a-126">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-126">Click **Edit**.</span></span>
20. <span data-ttu-id="e5f0a-127">Laajenna **Myynti**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="e5f0a-128">Syötä **Hinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="e5f0a-129">Tätä hintaa ei käytetä, jos soveltuvia kauppasopimuksia ei löydy.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="e5f0a-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-130">Click **Save**.</span></span>
23. <span data-ttu-id="e5f0a-131">Valitse **toimintoruudussa** **Myynti**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="e5f0a-132">Valitse **Luo kauppasopimukset**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="e5f0a-133">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-133">Click **New**.</span></span>
26. <span data-ttu-id="e5f0a-134">Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="e5f0a-135">Valitse luettelossa **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="e5f0a-136">Esittelytiedoissa **Commerce**-kirjauskansion nimi on **Hinta (myynti)** -suhteen oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="e5f0a-137">Tämä tarkoittaa sitä, että kaikkien uusien rivien oletusarvoina käytetään myyntihinnan kauppasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="e5f0a-138">Valitse **toimintoruudussa** **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="e5f0a-139">Valitse **Osapuolen koodityyppi** -kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="e5f0a-140">Avaa haku napsauttamalla **Tilin valinta** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="e5f0a-141">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="e5f0a-142">Tämä viimeistelee linkin kanavan, hintaryhmän ja kauppasopimuksen välillä.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="e5f0a-143">Syötä **Nimikkeen suhde** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="e5f0a-144">Lisää **Summa valuuttana** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="e5f0a-145">Valitse **Tiedot**-pikavälilehdessä **Etsi seuraava** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="e5f0a-146">Kun **Etsi seuraava** -kohdan arvoksi on määritetty Kyllä, hinnoittelumoduuli jatkaa sopivien alemman myyntihinnan omaavien kauppasopimusten etsimistä.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="e5f0a-147">Kun **Etsi seuraava** -kohdan arvoksi on määritetty Ei, hinnoittelumoduuli lopettaa etsimisen ja käyttää kauppasopimusta.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="e5f0a-148">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-148">Click **Post**.</span></span>
36. <span data-ttu-id="e5f0a-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-149">Click **OK**.</span></span>
37. <span data-ttu-id="e5f0a-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-150">Close the page.</span></span>
38. <span data-ttu-id="e5f0a-151">Valitse **toimintoruudussa** Myynti.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="e5f0a-152">Valitse **Myyntihinta**.</span><span class="sxs-lookup"><span data-stu-id="e5f0a-152">Click **Sales price**.</span></span>

