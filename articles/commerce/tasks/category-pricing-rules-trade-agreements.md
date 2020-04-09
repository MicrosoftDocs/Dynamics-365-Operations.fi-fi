---
title: Luokan hinnoittelusäännöt kauppasopimuksia varten
description: Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21b1986aa36aab23f50a5af434435f9e93318e45
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141080"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="dc1b0-103">Luokan hinnoittelusäännöt kauppasopimuksia varten</span><span class="sxs-lookup"><span data-stu-id="dc1b0-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc1b0-104">Tässä menettelyssä käsitellään, miten myyntihinnan kauppasopimukset luodaan luokan hinnoittelusääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="dc1b0-105">Tämän tehtävän luomisessa käytetty USRT-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="dc1b0-106">Tämä tehtävä on tarkoitettu kaupankäynnin myynninedistämispäällikön roolille.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="dc1b0-107">Valitse Hinnoittelun ja alennusten hallinta.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="dc1b0-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-108">Click New.</span></span>
3. <span data-ttu-id="dc1b0-109">Valitse Luokan hintasääntö.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-109">Click Category price rule.</span></span>
4. <span data-ttu-id="dc1b0-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="dc1b0-111">Valitse Tilikoodi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="dc1b0-112">Ryhmä-tyypin tilikoodilla määritetään kanava-, kanta-asiakasohjelma-, luettelo- ja liitoskohtaiset myyntihinnan kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="dc1b0-113">Anna tai valitse Tilin valinta -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="dc1b0-114">Anna tai valitse Luokka-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="dc1b0-115">Lisää Summa/prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="dc1b0-116">Anna tai valitse Pyöristysversio-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="dc1b0-117">Valitse Luo kauppasopimukset.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="dc1b0-118">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-118">Click Next.</span></span>
12. <span data-ttu-id="dc1b0-119">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="dc1b0-120">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="dc1b0-121">Valitse Etsi seuraava -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="dc1b0-122">Valitse Seuraava.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-122">Click Next.</span></span>
16. <span data-ttu-id="dc1b0-123">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-123">Click Finish.</span></span>
    * <span data-ttu-id="dc1b0-124">Luotu kauppasopimuksen kirjauskansio avautuu tarkistettavaksi.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="dc1b0-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc1b0-126">Luokan hinnoittelusäännöistä luotuja kauppasopimuksen kirjauskansioita ei kirjata.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="dc1b0-127">Voit tarkastella ja muokata luotuja hintoja ennen niiden kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="dc1b0-128">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-128">Click Edit.</span></span>
19. <span data-ttu-id="dc1b0-129">Lisää Summa valuuttana -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="dc1b0-130">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-130">Click Post.</span></span>
21. <span data-ttu-id="dc1b0-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-131">Click OK.</span></span>
22. <span data-ttu-id="dc1b0-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-132">Close the page.</span></span>
23. <span data-ttu-id="dc1b0-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-133">Close the page.</span></span>
24. <span data-ttu-id="dc1b0-134">Valitse Luokan hintasäännöt -välilehti.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="dc1b0-135">Kanavakohtaiset luokan hinnoittelusäännöt näkyvät tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dc1b0-135">Channel specific Category pricing rules will show in this list.</span></span>  

