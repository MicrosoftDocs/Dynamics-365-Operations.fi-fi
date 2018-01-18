--- 
title: "Määritä luottokorttien käsittely"
description: "Tässä menettelyssä kerrotaan, miten maksupalveluiden tarjoajien luetteloa tarkastellaan ja miten ostoreskontran maksutili määritetään."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 312ef54d8f9b2cff9b7d18916f5747c03148a063
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="7d309-103">Määritä luottokorttien käsittely</span><span class="sxs-lookup"><span data-stu-id="7d309-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7d309-104">Tässä menettelyssä kerrotaan, miten maksupalveluiden tarjoajien luetteloa tarkastellaan ja miten ostoreskontran maksutili määritetään.</span><span class="sxs-lookup"><span data-stu-id="7d309-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="7d309-105">Tässä menettelyssä käytetään esittelytietojen USRT-yritystä. Tämä on tarkoitettu järjestelmänvalvojille ja IT-asiantuntijoille.</span><span class="sxs-lookup"><span data-stu-id="7d309-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="7d309-106">Näytä maksupalveluiden tarjoajien luettelo</span><span class="sxs-lookup"><span data-stu-id="7d309-106">View a list of payment providers</span></span>
1. <span data-ttu-id="7d309-107">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksupalvelut.</span><span class="sxs-lookup"><span data-stu-id="7d309-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="7d309-108">Valitse Näytä käytettävissä olevat tarjoajat.</span><span class="sxs-lookup"><span data-stu-id="7d309-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="7d309-109">Määritä maksutili</span><span class="sxs-lookup"><span data-stu-id="7d309-109">Configure payment account</span></span>
1. <span data-ttu-id="7d309-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7d309-110">Click New.</span></span>
2. <span data-ttu-id="7d309-111">Syötä arvo Maksupalvelu-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d309-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="7d309-112">Valitse vaihtoehto Maksuyhdistin-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7d309-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="7d309-113">Ota käyttöön Maksupalvelutili-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="7d309-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="7d309-114">Syötä Ympäristö-kenttään TUOT.</span><span class="sxs-lookup"><span data-stu-id="7d309-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="7d309-115">Valitse Luottokorttityypit.</span><span class="sxs-lookup"><span data-stu-id="7d309-115">Click Credit card types.</span></span>
7. <span data-ttu-id="7d309-116">Avaa haku valitsemalla Maksukirjauskansio-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7d309-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7d309-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7d309-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7d309-118">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7d309-118">Click Add.</span></span>
10. <span data-ttu-id="7d309-119">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d309-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="7d309-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7d309-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7d309-121">Avaa haku valitsemalla Maksukirjauskansio-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7d309-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="7d309-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7d309-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7d309-123">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7d309-123">Click Add.</span></span>
15. <span data-ttu-id="7d309-124">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d309-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="7d309-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7d309-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7d309-126">Voit toistaa nämä vaiheet haluamallesi määrälle korttityyppejä.</span><span class="sxs-lookup"><span data-stu-id="7d309-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="7d309-127">Avaa haku valitsemalla Maksukirjauskansio-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7d309-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="7d309-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7d309-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="7d309-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="7d309-129">Click Add.</span></span>
20. <span data-ttu-id="7d309-130">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7d309-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="7d309-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7d309-131">Click Save.</span></span>
22. <span data-ttu-id="7d309-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7d309-132">Close the page.</span></span>
23. <span data-ttu-id="7d309-133">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="7d309-133">Click Validate.</span></span>
24. <span data-ttu-id="7d309-134">Valitse Uusien luottokorttien oletuskäsittelijä -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7d309-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="7d309-135">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7d309-135">Click Save.</span></span>


