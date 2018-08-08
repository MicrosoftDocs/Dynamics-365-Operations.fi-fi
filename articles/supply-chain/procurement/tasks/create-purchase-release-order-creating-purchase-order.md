--- 
title: Oston vapautustilauksen luominen ostotilausta luotaessa
description: "Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ad74f52682627d6164270de54e2dbcaeb57111fe
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="45261-103">Oston vapautustilauksen luominen ostotilausta luotaessa</span><span class="sxs-lookup"><span data-stu-id="45261-103">Create a purchase release order when creating the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45261-104">Tässä menettelyssä selvitetään, miten ostosopimusta voi käyttää ostotilauksen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="45261-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="45261-105">Ostosopimusta on käytettävä ostotilauksen luomiseen, koska sen yleisehdot on kopioitava ostotilauksen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="45261-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="45261-106">Yleensä ostoedustaja tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="45261-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="45261-107">Ennen tämän opastuksen käyttöä tarvitset voimassaolevan ostosopimuksen, jossa on toimittajan tuotemääräsitoutuminen ja nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="45261-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="45261-108">Samaa menettelyä voidaan käyttää, jos sinulla muun tyyppisiä sitoutumisia sisältävä ostosopimus.</span><span class="sxs-lookup"><span data-stu-id="45261-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="45261-109">Voit suorittaa tämän ohjauksen esittely-tietojen USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="45261-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="45261-110">Jos käytössä on USMF, määritä tämän opastuksen tarvitsemat ennakkoehdot suorittamalla ensin ostosopimuksen luontiopastus.</span><span class="sxs-lookup"><span data-stu-id="45261-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="45261-111">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="45261-111">Create a purchase order</span></span>
1. <span data-ttu-id="45261-112">Avaa ostotilauksen valmistelun työtila.</span><span class="sxs-lookup"><span data-stu-id="45261-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="45261-113">Valitse Uusi ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="45261-113">Click New purchase order.</span></span>
3. <span data-ttu-id="45261-114">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45261-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="45261-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45261-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="45261-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45261-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="45261-117">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="45261-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="45261-118">Avaa haku napsauttamalla Ostosopimus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="45261-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="45261-119">Kaikki toiminnot käytettävissä olevat sopimukset ovat tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="45261-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="45261-120">Etsi voimassaoleva sopimus, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="45261-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="45261-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45261-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="45261-122">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="45261-122">Click Yes.</span></span>
10. <span data-ttu-id="45261-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="45261-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="45261-124">Lisää rivi</span><span class="sxs-lookup"><span data-stu-id="45261-124">Add a line</span></span>
1. <span data-ttu-id="45261-125">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45261-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="45261-126">Jos sitoutumisessa on tietty varasto- tai toimipaikkasijainti, samat arvot on annettava ostotilausriville, jotta sopimusta voisi käyttää.</span><span class="sxs-lookup"><span data-stu-id="45261-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="45261-127">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="45261-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="45261-128">Sijainti on ehkä jo täytetty tilauksen tai toimittajan oletusarvolla.</span><span class="sxs-lookup"><span data-stu-id="45261-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="45261-129">Voit siinä tapauksessa ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="45261-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="45261-130">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45261-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="45261-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45261-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="45261-132">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45261-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="45261-133">Tarkista, että hinta on kopioitu sitoutumisesta.</span><span class="sxs-lookup"><span data-stu-id="45261-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="45261-134">Hae sitoutuminen</span><span class="sxs-lookup"><span data-stu-id="45261-134">Look up the commitment</span></span>
1. <span data-ttu-id="45261-135">Valitse Päivitä rivi.</span><span class="sxs-lookup"><span data-stu-id="45261-135">Click Update line.</span></span>
2. <span data-ttu-id="45261-136">Valitse Liitetty.</span><span class="sxs-lookup"><span data-stu-id="45261-136">Click Attached.</span></span>
    * <span data-ttu-id="45261-137">Tässä on lisätietoja ostosopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="45261-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="45261-138">Näet esimerkiksi hinnan ja tiedon siitä, ovatko hinta ja alennus kiinteitä. Jos näin on ja vaihdat hinnan tai alennuksen ostotilauksessa sitoutumisesta poikkeavaan hintaan, järjestelmä poistaa linkin, jolloin ostotilausrivi ei täytä sitoutumista.</span><span class="sxs-lookup"><span data-stu-id="45261-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="45261-139">Näet myös, onko Maksimi pakotetaan -vaihtoehto valittu. Jos näin on, sitoutumisen määrää ei voi ylittää, kun kaikki sitoutumisen täyttävät ostot lasketaan yhteen.</span><span class="sxs-lookup"><span data-stu-id="45261-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="45261-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="45261-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="45261-141">Hae ostosopimus</span><span class="sxs-lookup"><span data-stu-id="45261-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="45261-142">Valitse toimintoruudussa Yleiset.</span><span class="sxs-lookup"><span data-stu-id="45261-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="45261-143">Valitse Ostosopimus.</span><span class="sxs-lookup"><span data-stu-id="45261-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="45261-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="45261-144">Close the page.</span></span>
4. <span data-ttu-id="45261-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="45261-145">Close the page.</span></span>


