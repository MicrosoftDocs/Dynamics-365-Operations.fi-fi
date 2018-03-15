--- 
title: Etukelpoisuusprosessi
description: "Tässä menettelyssä kerrotaan, miten edun kelpoisuuskäsittely toimii."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abc52192848649672cbcb8c770d74ba2aef139be
ms.openlocfilehash: fe773bd2375b2dea8e13a57918ad584f83f61073
ms.contentlocale: fi-fi
ms.lasthandoff: 02/14/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="922f4-103">Etukelpoisuusprosessi</span><span class="sxs-lookup"><span data-stu-id="922f4-103">Benefit eligibility process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="922f4-104">Tässä menettelyssä kerrotaan, miten edun kelpoisuuskäsittely toimii.</span><span class="sxs-lookup"><span data-stu-id="922f4-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="922f4-105">Voit käsittely on valmis, voit tarkastella tuloksia.</span><span class="sxs-lookup"><span data-stu-id="922f4-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="922f4-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="922f4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="922f4-107">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="922f4-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="922f4-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="922f4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="922f4-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="922f4-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="922f4-110">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="922f4-110">Click Edit.</span></span>
5. <span data-ttu-id="922f4-111">Valitse Oikeutus-kentässä Sääntöön perustuva.</span><span class="sxs-lookup"><span data-stu-id="922f4-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="922f4-112">Valitse Sääntötyyppi-kentässä edussa käytettävä käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="922f4-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="922f4-113">Valitse toimintoruudussa Etu.</span><span class="sxs-lookup"><span data-stu-id="922f4-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="922f4-114">Avaa valintaikkuna valitsemalla Luo kelpoisuustapahtuma.</span><span class="sxs-lookup"><span data-stu-id="922f4-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="922f4-115">Kirjoita Tapahtuma-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="922f4-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="922f4-116">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="922f4-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="922f4-117">Valitse Tapahtumatyyppi-kentässä Avaa rekisteröinti.</span><span class="sxs-lookup"><span data-stu-id="922f4-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="922f4-118">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="922f4-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="922f4-119">Anna Rekisteröitymisaika-kentässä päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="922f4-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="922f4-120">Lisää Rekisteröitymispäivät-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="922f4-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="922f4-121">Valitse Luo tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="922f4-121">Click Create event.</span></span>
16. <span data-ttu-id="922f4-122">Valitse Työntekijät-pikavälilehdessä Lisää.</span><span class="sxs-lookup"><span data-stu-id="922f4-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="922f4-123">Valitse Tarkastele tyypin mukaan -kentässä Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="922f4-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="922f4-124">Valitse Tarkastele oikeushenkilön mukaan -kentässä Valittu yritys.</span><span class="sxs-lookup"><span data-stu-id="922f4-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="922f4-125">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="922f4-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="922f4-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="922f4-126">Click OK.</span></span>
21. <span data-ttu-id="922f4-127">Valitse Prosessi.</span><span class="sxs-lookup"><span data-stu-id="922f4-127">Click Process.</span></span>
22. <span data-ttu-id="922f4-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="922f4-128">Click OK.</span></span>
23. <span data-ttu-id="922f4-129">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="922f4-129">Refresh the page.</span></span>
24. <span data-ttu-id="922f4-130">Valitse Näytä tulokset.</span><span class="sxs-lookup"><span data-stu-id="922f4-130">Click Show results.</span></span>
25. <span data-ttu-id="922f4-131">Avaa Tila-sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="922f4-131">Open Status column filter.</span></span>
26. <span data-ttu-id="922f4-132">Lajittele A–Z</span><span class="sxs-lookup"><span data-stu-id="922f4-132">Sort A to Z</span></span>


