--- 
title: "Luokan hinnoittelusäännöt kauppasopimuksia varten"
description: "Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla."
author: scott-tucker
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 454f74627bd4811fa657b0c6b06003a8fdbdb599
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="f95b4-103">Luokan hinnoittelusäännöt kauppasopimuksia varten</span><span class="sxs-lookup"><span data-stu-id="f95b4-103">Category pricing rules to create trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f95b4-104">Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="f95b4-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="f95b4-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="f95b4-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f95b4-106">Tämä tehtävä on tarkoitettu vähittäismyynnin myynninedistämispäällikön roolille.</span><span class="sxs-lookup"><span data-stu-id="f95b4-106">This task is intended for the Retail merchandising manager role.</span></span>

1. <span data-ttu-id="f95b4-107">Valitse Hinnoittelun ja alennusten hallinta.</span><span class="sxs-lookup"><span data-stu-id="f95b4-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="f95b4-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f95b4-108">Click New.</span></span>
3. <span data-ttu-id="f95b4-109">Valitse Luokan hintasääntö.</span><span class="sxs-lookup"><span data-stu-id="f95b4-109">Click Category price rule.</span></span>
4. <span data-ttu-id="f95b4-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f95b4-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="f95b4-111">Valitse Tilikoodi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f95b4-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="f95b4-112">Ryhmä-tyypin tilikoodilla määritetään kanava-, kanta-asiakasohjelma-, luettelo- ja liitoskohtaiset myyntihinnan kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="f95b4-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="f95b4-113">Anna tai valitse Tilin valinta -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f95b4-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="f95b4-114">Anna tai valitse Luokka-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f95b4-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="f95b4-115">Lisää Summa/prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f95b4-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="f95b4-116">Anna tai valitse Pyöristysversio-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f95b4-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="f95b4-117">Valitse Luo kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="f95b4-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="f95b4-118">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="f95b4-118">Click Next.</span></span>
12. <span data-ttu-id="f95b4-119">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f95b4-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="f95b4-120">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f95b4-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="f95b4-121">Valitse Etsi seuraava -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="f95b4-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="f95b4-122">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="f95b4-122">Click Next.</span></span>
16. <span data-ttu-id="f95b4-123">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="f95b4-123">Click Finish.</span></span>
    * <span data-ttu-id="f95b4-124">Luotu kauppasopimuksen kirjauskansio avautuu tarkistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="f95b4-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="f95b4-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f95b4-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f95b4-126">Luokan hinnoittelusäännöistä luotuja kauppasopimuksen kirjauskansioita ei kirjata.</span><span class="sxs-lookup"><span data-stu-id="f95b4-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="f95b4-127">Voit tarkastella ja muokata luotuja hintoja ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="f95b4-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="f95b4-128">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="f95b4-128">Click Edit.</span></span>
19. <span data-ttu-id="f95b4-129">Lisää Summa valuuttana -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f95b4-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="f95b4-130">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="f95b4-130">Click Post.</span></span>
21. <span data-ttu-id="f95b4-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f95b4-131">Click OK.</span></span>
22. <span data-ttu-id="f95b4-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95b4-132">Close the page.</span></span>
23. <span data-ttu-id="f95b4-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f95b4-133">Close the page.</span></span>
24. <span data-ttu-id="f95b4-134">Valitse Luokan hintasäännöt -välilehti.</span><span class="sxs-lookup"><span data-stu-id="f95b4-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="f95b4-135">Kanavakohtaiset luokan hinnoittelusäännöt näkyvät tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f95b4-135">Channel specific Category pricing rules will show in this list.</span></span>  


