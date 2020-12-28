---
title: Vähittäismyynnin hinnanoikaisut
description: Tässä menettelyssä esitellään kaupan hinnanoikaisun luominen.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83498fa0a0432cb182106d6d273cb6117ed0b094
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412006"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="7c1f4-103">Vähittäismyynnin hinnanoikaisut</span><span class="sxs-lookup"><span data-stu-id="7c1f4-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c1f4-104">Tässä menettelyssä esitellään kaupan hinnanoikaisun luominen.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="7c1f4-105">Hinnanoikaisu voidaan määrittää suoraan nimikkeen myyntihinnalle. Vaihtoehtoisesti myös perusmyyntihintaa tai kauppasopimuksen myyntihintaa voidaan muokata.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="7c1f4-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="7c1f4-107">Valitse Hinnoittelun ja alennusten hallinta.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="7c1f4-108">Valitse Hinnanoikaisut-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="7c1f4-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-109">Click New.</span></span>
    * <span data-ttu-id="7c1f4-110">Tässä voit luoda kaikki useimmiten käytetyt hintojen ja alennusten säännöt, kuten alennukset, hinnanoikaisut, kauppasopimuksen kirjauskansiot ja luokan hinnoittelusäännöt.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="7c1f4-111">Valitse Hinnanoikaisu.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="7c1f4-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="7c1f4-113">Laajenna Rivit-osa.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="7c1f4-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-114">Click Add.</span></span>
    * <span data-ttu-id="7c1f4-115">Syötä tässä esimerkissä Tuote-kenttään arvo 81126.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="7c1f4-116">Syötä sitten Alennusprosentti-kenttään 10,0.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="7c1f4-117">Alennusprosentti-tyyppinen hinnanoikaisu pienentää perusmyyntihintaa tai kauppasopimuksen myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="7c1f4-118">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-118">Click Add.</span></span>
    * <span data-ttu-id="7c1f4-119">Anna tässä esimerkissä Tuote-kenttään arvo 81125.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="7c1f4-120">Valitse sitten Alennustapa-kenttään Käteisalennussumma.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="7c1f4-121">Syötä lopuksi Käteisalennussumma-kenttään 5,0.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="7c1f4-122">Käteisalennussumman alennuksen tyyppi on summa, joka saadaan perushinnasta tai kauppasopimuksen hinnasta.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="7c1f4-123">Valitse Hintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-123">Click Price groups.</span></span>
    * <span data-ttu-id="7c1f4-124">Valitse Hintaryhmä-kenttään RP-Houston.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="7c1f4-125">Tämä liittää hinnanoikaisun Houstonin myymälään.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="7c1f4-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-126">Click Save.</span></span>
11. <span data-ttu-id="7c1f4-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-127">Close the page.</span></span>
12. <span data-ttu-id="7c1f4-128">Valitse Tila-kentässä Käytössä.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="7c1f4-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-129">Click Save.</span></span>
14. <span data-ttu-id="7c1f4-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-130">Close the page.</span></span>
15. <span data-ttu-id="7c1f4-131">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="7c1f4-131">Refresh the page.</span></span>

