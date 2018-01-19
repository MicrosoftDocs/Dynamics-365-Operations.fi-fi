--- 
title: "Luokan hinnoittelusäännöt kauppasopimuksia varten"
description: "Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 4c67b3d24504f0f1c884b52598150cc5751afc5b
ms.contentlocale: fi-fi
ms.lasthandoff: 01/19/2018

---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="e8496-103">Luokan hinnoittelusäännöt kauppasopimuksia varten</span><span class="sxs-lookup"><span data-stu-id="e8496-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e8496-104">Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="e8496-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="e8496-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="e8496-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="e8496-106">Tämä tehtävä on tarkoitettu vähittäismyynnin myynninedistämispäällikön roolille.</span><span class="sxs-lookup"><span data-stu-id="e8496-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="e8496-107">Valitse Hinnoittelun ja alennusten hallinta.</span><span class="sxs-lookup"><span data-stu-id="e8496-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="e8496-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e8496-108">Click New.</span></span>
3. <span data-ttu-id="e8496-109">Valitse Luokan hintasääntö.</span><span class="sxs-lookup"><span data-stu-id="e8496-109">Click Category price rule.</span></span>
4. <span data-ttu-id="e8496-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e8496-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="e8496-111">Valitse Tilikoodi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="e8496-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="e8496-112">Ryhmä-tyypin tilikoodilla määritetään kanava-, kanta-asiakasohjelma-, luettelo- ja liitoskohtaiset myyntihinnan kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="e8496-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="e8496-113">Anna tai valitse Tilin valinta -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8496-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="e8496-114">Anna tai valitse Luokka-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8496-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="e8496-115">Lisää Summa/prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e8496-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="e8496-116">Anna tai valitse Pyöristysversio-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e8496-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="e8496-117">Valitse Luo kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="e8496-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="e8496-118">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="e8496-118">Click Next.</span></span>
12. <span data-ttu-id="e8496-119">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e8496-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="e8496-120">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e8496-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="e8496-121">Valitse Etsi seuraava -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e8496-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="e8496-122">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="e8496-122">Click Next.</span></span>
16. <span data-ttu-id="e8496-123">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="e8496-123">Click Finish.</span></span>
    * <span data-ttu-id="e8496-124">Luotu kauppasopimuksen kirjauskansio avautuu tarkistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="e8496-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="e8496-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e8496-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e8496-126">Luokan hinnoittelusäännöistä luotuja kauppasopimuksen kirjauskansioita ei kirjata.</span><span class="sxs-lookup"><span data-stu-id="e8496-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="e8496-127">Voit tarkastella ja muokata luotuja hintoja ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="e8496-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="e8496-128">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e8496-128">Click Edit.</span></span>
19. <span data-ttu-id="e8496-129">Lisää Summa valuuttana -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e8496-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="e8496-130">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="e8496-130">Click Post.</span></span>
21. <span data-ttu-id="e8496-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e8496-131">Click OK.</span></span>
22. <span data-ttu-id="e8496-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e8496-132">Close the page.</span></span>
23. <span data-ttu-id="e8496-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e8496-133">Close the page.</span></span>
24. <span data-ttu-id="e8496-134">Valitse Luokan hintasäännöt -välilehti.</span><span class="sxs-lookup"><span data-stu-id="e8496-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="e8496-135">Kanavakohtaiset luokan hinnoittelusäännöt näkyvät tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e8496-135">Channel specific Category pricing rules will show in this list.</span></span>  


