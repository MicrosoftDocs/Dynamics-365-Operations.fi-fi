---
title: Määritä työn ja kulujen vakiokustannukset
description: Tämä menettely osoittaa, miten projektin työn ja kulujen standardikustannukset määritetään.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572393"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="b555b-103">Määritä työn ja kulujen vakiokustannukset</span><span class="sxs-lookup"><span data-stu-id="b555b-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b555b-104">Tämä menettely osoittaa, miten projektin työn ja kulujen standardikustannukset määritetään.</span><span class="sxs-lookup"><span data-stu-id="b555b-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="b555b-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="b555b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b555b-106">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (tunti).</span><span class="sxs-lookup"><span data-stu-id="b555b-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="b555b-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b555b-107">Click New.</span></span>
3. <span data-ttu-id="b555b-108">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b555b-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="b555b-109">Syötä Kustannushinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b555b-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="b555b-110">Voit määrittää projektiluokalle standardikustannushinnan. Vaihtoehtoisesti voit määrittää kustannushinnan työntekijänumeron, projektin numeron, luokan, päivämäärän tai näiden yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="b555b-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="b555b-111">Käytettävä kustannushinta on tarkimmin määritetty kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="b555b-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="b555b-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b555b-112">Click Save.</span></span>
6. <span data-ttu-id="b555b-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b555b-113">Close the page.</span></span>
7. <span data-ttu-id="b555b-114">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (tunti).</span><span class="sxs-lookup"><span data-stu-id="b555b-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="b555b-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b555b-115">Click New.</span></span>
9. <span data-ttu-id="b555b-116">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b555b-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="b555b-117">Valitse Kirjaustapa-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b555b-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="b555b-118">Anna Hinnoittelu-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="b555b-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="b555b-119">Voit määrittää vakiomyyntihinnan tuntitapahtumille, projektiluokalle.</span><span class="sxs-lookup"><span data-stu-id="b555b-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="b555b-120">Voit määrittää myyntihinnat myös työntekijänumeron, projektinumeron, luokan, tapahtumapäivämäärän tai näiden yhdistelmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="b555b-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="b555b-121">Varsinainen myyntihinta, jota käytetään työntekijän kirjatessa tapahtuman tuntikirjauskansioon, on se hinta, josta on yksityiskohtaisimmat tiedot.</span><span class="sxs-lookup"><span data-stu-id="b555b-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b555b-122">Jos määritetään esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta, työntekijäkohtaista myyntihintaa käytetään.</span><span class="sxs-lookup"><span data-stu-id="b555b-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="b555b-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b555b-123">Click Save.</span></span>
13. <span data-ttu-id="b555b-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b555b-124">Close the page.</span></span>
14. <span data-ttu-id="b555b-125">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (kulu).</span><span class="sxs-lookup"><span data-stu-id="b555b-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="b555b-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b555b-126">Click New.</span></span>
16. <span data-ttu-id="b555b-127">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b555b-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="b555b-128">Syötä Kustannushinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b555b-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="b555b-129">Useita kenttiä voidaan täyttää, mutta tämä on tietueen tallentamiseen tarvittava minimimäärä.</span><span class="sxs-lookup"><span data-stu-id="b555b-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="b555b-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b555b-130">Click Save.</span></span>
19. <span data-ttu-id="b555b-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b555b-131">Close the page.</span></span>
20. <span data-ttu-id="b555b-132">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (kulu).</span><span class="sxs-lookup"><span data-stu-id="b555b-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="b555b-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b555b-133">Click New.</span></span>
22. <span data-ttu-id="b555b-134">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b555b-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="b555b-135">Valitse Kirjaustapa-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b555b-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="b555b-136">Anna Hinnoittelu-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="b555b-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="b555b-137">Todellinen myyntihinta, jota käytetään, kun työntekijä kirjaa tapahtumia kulukirjauskansioon, on yksityiskohtaisimmat tiedot omaava myyntihinta.</span><span class="sxs-lookup"><span data-stu-id="b555b-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b555b-138">Jos esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta määritetään, käytetään työntekijäkohtaista myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="b555b-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="b555b-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b555b-139">Click Save.</span></span>

