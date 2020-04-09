---
title: Määritä työn ja kulujen vakiokustannukset
description: Tässä aiheessa kerrotaan, miten projektin työn ja kulujen standardikustannukset määritetään.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140090"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="c06b3-103">Määritä työn ja kulujen vakiokustannukset</span><span class="sxs-lookup"><span data-stu-id="c06b3-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c06b3-104">Tässä aiheessa kerrotaan, miten projektin työn ja kulujen standardikustannukset määritetään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="c06b3-105">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="c06b3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c06b3-106">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (tunti).**</span><span class="sxs-lookup"><span data-stu-id="c06b3-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="c06b3-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-107">Select **New**.</span></span>
3. <span data-ttu-id="c06b3-108">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="c06b3-109">Syötä **Kustannushinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c06b3-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c06b3-110">Voit määrittää projektiluokalle standardikustannushinnan. Vaihtoehtoisesti voit määrittää kustannushinnan työntekijänumeron, projektin numeron, luokan, päivämäärän tai näiden yhdistelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="c06b3-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="c06b3-111">Käytettävä kustannushinta on tarkimmin määritetty kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="c06b3-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="c06b3-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-112">Select **Save**.</span></span>
6. <span data-ttu-id="c06b3-113">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (tunti).**</span><span class="sxs-lookup"><span data-stu-id="c06b3-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="c06b3-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-114">Select **New**.</span></span>
8. <span data-ttu-id="c06b3-115">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="c06b3-116">Valitse **Kirjaustapa**-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c06b3-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="c06b3-117">Anna **Hinnoittelu**-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="c06b3-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c06b3-118">Voit määrittää vakiomyyntihinnan tuntitapahtumille, projektiluokalle.</span><span class="sxs-lookup"><span data-stu-id="c06b3-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="c06b3-119">Voit määrittää myyntihinnat myös työntekijänumeron, projektinumeron, luokan, tapahtumapäivämäärän tai näiden yhdistelmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="c06b3-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="c06b3-120">Varsinainen myyntihinta, jota käytetään työntekijän kirjatessa tapahtuman tuntikirjauskansioon, on se hinta, josta on yksityiskohtaisimmat tiedot.</span><span class="sxs-lookup"><span data-stu-id="c06b3-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c06b3-121">Jos määritetään esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta, työntekijäkohtaista myyntihintaa käytetään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="c06b3-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-122">Select **Save**.</span></span>
12. <span data-ttu-id="c06b3-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c06b3-123">Close the page.</span></span>
13. <span data-ttu-id="c06b3-124">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Kustannushinta (kulu).**</span><span class="sxs-lookup"><span data-stu-id="c06b3-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="c06b3-125">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-125">Select **New**.</span></span>
15. <span data-ttu-id="c06b3-126">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="c06b3-127">Syötä **Kustannushinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c06b3-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c06b3-128">Useita kenttiä voidaan täyttää, mutta tämä on tietueen tallentamiseen tarvittava minimimäärä.</span><span class="sxs-lookup"><span data-stu-id="c06b3-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="c06b3-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-129">Select **Save**.</span></span>
18. <span data-ttu-id="c06b3-130">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Asetukset > Hinnat > Myyntihinta (kulu).**</span><span class="sxs-lookup"><span data-stu-id="c06b3-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="c06b3-131">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-131">Select **New**.</span></span>
20. <span data-ttu-id="c06b3-132">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c06b3-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="c06b3-133">Valitse **Kirjaustapa**-kentästä jokin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c06b3-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="c06b3-134">Anna **Hinnoittelu**-kentässä luku.</span><span class="sxs-lookup"><span data-stu-id="c06b3-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c06b3-135">Todellinen myyntihinta, jota käytetään, kun työntekijä kirjaa tapahtumia kulukirjauskansioon, on yksityiskohtaisimmat tiedot omaava myyntihinta.</span><span class="sxs-lookup"><span data-stu-id="c06b3-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c06b3-136">Jos esimerkiksi sekä yleinen että työntekijäkohtainen myyntihinta määritetään, käytetään työntekijäkohtaista myyntihintaa.</span><span class="sxs-lookup"><span data-stu-id="c06b3-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="c06b3-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c06b3-137">Select **Save**.</span></span>

