--- 
title: Perushinta ja kauppasopimukset
description: "Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen."
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: cdbbf4db6ce9e33e4cb6e31d74cd0a62f5666873
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="d744a-103">Perushinta ja kauppasopimukset</span><span class="sxs-lookup"><span data-stu-id="d744a-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d744a-104">Tässä menettelyssä esitellään kanavakohtaisen myyntihinnan kauppasopimusten luominen.</span><span class="sxs-lookup"><span data-stu-id="d744a-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="d744a-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="d744a-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="d744a-106">Siirry kohtaan Vähittäismyynti ja kauppa > Hinnoittelu ja alennukset > Hintaryhmät > Kaikki hintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="d744a-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="d744a-107">Hintaryhmät tarkoittava tapaa, jolla kauppasopimukset on liitetty tiettyihin kanaviin.</span><span class="sxs-lookup"><span data-stu-id="d744a-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="d744a-108">Jos hintaryhmiä käytetään kauppasopimusten liittämisessä kanaviin, käytössä on kanavakohtainen hinnoittelu.</span><span class="sxs-lookup"><span data-stu-id="d744a-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="d744a-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d744a-109">Click New.</span></span>
3. <span data-ttu-id="d744a-110">Syötä arvo Hintaryhmät-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d744a-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="d744a-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d744a-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d744a-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d744a-112">Click Save.</span></span>
6. <span data-ttu-id="d744a-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d744a-113">Close the page.</span></span>
7. <span data-ttu-id="d744a-114">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälät > Kaikki vähittäismyymälät.</span><span class="sxs-lookup"><span data-stu-id="d744a-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="d744a-115">Valitse luettelosta New York.</span><span class="sxs-lookup"><span data-stu-id="d744a-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="d744a-116">Valitse toimintoruudussa Myymälä.</span><span class="sxs-lookup"><span data-stu-id="d744a-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="d744a-117">Valitse Hintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="d744a-117">Click Price groups.</span></span>
11. <span data-ttu-id="d744a-118">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d744a-118">Click New.</span></span>
12. <span data-ttu-id="d744a-119">Avaa haku valitsemalla Hintaryhmät-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d744a-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="d744a-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d744a-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d744a-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d744a-121">Click Save.</span></span>
15. <span data-ttu-id="d744a-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d744a-122">Close the page.</span></span>
16. <span data-ttu-id="d744a-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d744a-123">Close the page.</span></span>
17. <span data-ttu-id="d744a-124">Siirry kohtaan Vähittäismyynti ja kauppa > Tuotteet ja luokat > Vapautetut tuotteet luokittain.</span><span class="sxs-lookup"><span data-stu-id="d744a-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="d744a-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d744a-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="d744a-126">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="d744a-126">Click Edit.</span></span>
20. <span data-ttu-id="d744a-127">Ota käyttöön Myynti-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="d744a-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="d744a-128">Syötä Hinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="d744a-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="d744a-129">Tätä hintaa ei käytetä, jos soveltuvia kauppasopimuksia ei löydy.</span><span class="sxs-lookup"><span data-stu-id="d744a-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="d744a-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d744a-130">Click Save.</span></span>
23. <span data-ttu-id="d744a-131">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="d744a-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="d744a-132">Valitse Luo kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="d744a-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="d744a-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d744a-133">Click New.</span></span>
26. <span data-ttu-id="d744a-134">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d744a-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="d744a-135">Valitse luettelosta Vähittäismyynti.</span><span class="sxs-lookup"><span data-stu-id="d744a-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="d744a-136">Esittelytiedoissa Vähittäismyynti-kirjauskansion nimi on Hinta (myynti) -suhteen oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="d744a-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="d744a-137">Tämä tarkoittaa sitä, että kaikkien uusien rivien oletusarvoina käytetään myyntihinnan kauppasopimuksia.</span><span class="sxs-lookup"><span data-stu-id="d744a-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="d744a-138">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="d744a-138">Click Lines.</span></span>
29. <span data-ttu-id="d744a-139">Valitse Tilikoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="d744a-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="d744a-140">Avaa haku napsauttamalla Tilin valinta -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d744a-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="d744a-141">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d744a-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d744a-142">Tämä viimeistelee linkin kanavan, hintaryhmän ja kauppasopimuksen välillä.</span><span class="sxs-lookup"><span data-stu-id="d744a-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="d744a-143">Syötä Nimikkeen suhde -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="d744a-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="d744a-144">Lisää Summa valuuttana -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="d744a-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="d744a-145">Valitse Etsi seuraava -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="d744a-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="d744a-146">Kun Etsi seuraava -kohdan arvoksi on määritetty Kyllä, hinnoittelumoduuli jatkaa sopivien alemman myyntihinnan omaavien kauppasopimusten etsimistä.</span><span class="sxs-lookup"><span data-stu-id="d744a-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="d744a-147">Kun Etsi seuraava -kohdan arvoksi on määritetty Ei, hinnoittelumoduuli lopettaa etsimisen ja käyttää kauppasopimusta.</span><span class="sxs-lookup"><span data-stu-id="d744a-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="d744a-148">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="d744a-148">Click Post.</span></span>
36. <span data-ttu-id="d744a-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d744a-149">Click OK.</span></span>
37. <span data-ttu-id="d744a-150">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d744a-150">Close the page.</span></span>
38. <span data-ttu-id="d744a-151">Valitse toimintoruudussa Myynti.</span><span class="sxs-lookup"><span data-stu-id="d744a-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="d744a-152">Valitse Myyntihinta.</span><span class="sxs-lookup"><span data-stu-id="d744a-152">Click Sales price.</span></span>


