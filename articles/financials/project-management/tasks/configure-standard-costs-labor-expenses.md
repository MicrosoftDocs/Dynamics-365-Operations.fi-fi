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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845882"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="4dc8d-103">Määritä työn ja kulujen vakiokustannukset</span><span class="sxs-lookup"><span data-stu-id="4dc8d-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dc8d-104">Tämä menettely osoittaa, miten projektin työn ja kulujen standardikustannukset määritetään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="4dc8d-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4dc8d-106">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (tunti).</span><span class="sxs-lookup"><span data-stu-id="4dc8d-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="4dc8d-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-107">Click New.</span></span>
3. <span data-ttu-id="4dc8d-108">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="4dc8d-109">Syötä Kustannushinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="4dc8d-110">Voit määrittää projektiluokalle standardikustannushinnan. Vaihtoehtoisesti voit määrittää kustannushinnan työntekijänumeron, projektin numeron, luokan, päivämäärän tai näiden yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="4dc8d-111">Käytettävä kustannushinta on tarkimmin määritetty kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="4dc8d-112">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-112">Click Save.</span></span>
6. <span data-ttu-id="4dc8d-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-113">Close the page.</span></span>
7. <span data-ttu-id="4dc8d-114">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (tunti).</span><span class="sxs-lookup"><span data-stu-id="4dc8d-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="4dc8d-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-115">Click New.</span></span>
9. <span data-ttu-id="4dc8d-116">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="4dc8d-117">Valitse Kirjaustapa-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="4dc8d-118">Anna Hinnoittelu-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="4dc8d-119">Voit määrittää vakiomyyntihinnan tuntitapahtumille, projektiluokalle.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="4dc8d-120">Voit määrittää myyntihinnat myös työntekijänumeron, projektinumeron, luokan, tapahtumapäivämäärän tai näiden yhdistelmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="4dc8d-121">Varsinainen myyntihinta, jota käytetään työntekijän kirjatessa tapahtuman tuntikirjauskansioon, on se hinta, josta on yksityiskohtaisimmat tiedot.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4dc8d-122">Jos määritetään esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta, työntekijäkohtaista myyntihintaa käytetään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="4dc8d-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-123">Click Save.</span></span>
13. <span data-ttu-id="4dc8d-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-124">Close the page.</span></span>
14. <span data-ttu-id="4dc8d-125">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (kulu).</span><span class="sxs-lookup"><span data-stu-id="4dc8d-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="4dc8d-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-126">Click New.</span></span>
16. <span data-ttu-id="4dc8d-127">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="4dc8d-128">Syötä Kustannushinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="4dc8d-129">Useita kenttiä voidaan täyttää, mutta tämä on tietueen tallentamiseen tarvittava minimimäärä.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="4dc8d-130">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-130">Click Save.</span></span>
19. <span data-ttu-id="4dc8d-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-131">Close the page.</span></span>
20. <span data-ttu-id="4dc8d-132">Valitse Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (kulu).</span><span class="sxs-lookup"><span data-stu-id="4dc8d-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="4dc8d-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-133">Click New.</span></span>
22. <span data-ttu-id="4dc8d-134">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="4dc8d-135">Valitse Kirjaustapa-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="4dc8d-136">Anna Hinnoittelu-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="4dc8d-137">Todellinen myyntihinta, jota käytetään, kun työntekijä kirjaa tapahtumia kulukirjauskansioon, on yksityiskohtaisimmat tiedot omaava myyntihinta.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4dc8d-138">Jos esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta määritetään, käytetään työntekijäkohtaista myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="4dc8d-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4dc8d-139">Click Save.</span></span>

