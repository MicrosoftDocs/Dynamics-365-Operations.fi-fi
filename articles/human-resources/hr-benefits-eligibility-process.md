---
title: Etukelpoisuusprosessi
description: Tässä menettelyssä kerrotaan, miten edun kelpoisuuskäsittely toimii.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 57e3e1dde4b4c8038b151dabf17af0f911f2ba07
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008903"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="43f17-103">Etukelpoisuusprosessi</span><span class="sxs-lookup"><span data-stu-id="43f17-103">Benefit eligibility process</span></span>

<span data-ttu-id="43f17-104">Tässä menettelyssä kerrotaan, miten edun kelpoisuuskäsittely toimii.</span><span class="sxs-lookup"><span data-stu-id="43f17-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="43f17-105">Voit käsittely on valmis, voit tarkastella tuloksia.</span><span class="sxs-lookup"><span data-stu-id="43f17-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="43f17-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="43f17-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="43f17-107">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="43f17-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="43f17-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="43f17-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="43f17-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="43f17-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="43f17-110">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="43f17-110">Click Edit.</span></span>
5. <span data-ttu-id="43f17-111">Valitse Oikeutus-kentässä Sääntöön perustuva.</span><span class="sxs-lookup"><span data-stu-id="43f17-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="43f17-112">Valitse Sääntötyyppi-kentässä edussa käytettävä käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="43f17-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="43f17-113">Valitse toimintoruudussa Etu.</span><span class="sxs-lookup"><span data-stu-id="43f17-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="43f17-114">Avaa valintaikkuna valitsemalla Luo kelpoisuustapahtuma.</span><span class="sxs-lookup"><span data-stu-id="43f17-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="43f17-115">Kirjoita Tapahtuma-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="43f17-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="43f17-116">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="43f17-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="43f17-117">Valitse Tapahtumatyyppi-kentässä Avaa rekisteröinti.</span><span class="sxs-lookup"><span data-stu-id="43f17-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="43f17-118">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="43f17-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="43f17-119">Anna Rekisteröitymisaika-kentässä päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="43f17-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="43f17-120">Lisää Rekisteröitymispäivät-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="43f17-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="43f17-121">Valitse Luo tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="43f17-121">Click Create event.</span></span>
16. <span data-ttu-id="43f17-122">Valitse Työntekijät-pikavälilehdessä Lisää.</span><span class="sxs-lookup"><span data-stu-id="43f17-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="43f17-123">Valitse Tarkastele tyypin mukaan -kentässä Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="43f17-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="43f17-124">Valitse Tarkastele oikeushenkilön mukaan -kentässä Valittu yritys.</span><span class="sxs-lookup"><span data-stu-id="43f17-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="43f17-125">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="43f17-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="43f17-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="43f17-126">Click OK.</span></span>
21. <span data-ttu-id="43f17-127">Valitse Prosessi.</span><span class="sxs-lookup"><span data-stu-id="43f17-127">Click Process.</span></span>
22. <span data-ttu-id="43f17-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="43f17-128">Click OK.</span></span>
23. <span data-ttu-id="43f17-129">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="43f17-129">Refresh the page.</span></span>
24. <span data-ttu-id="43f17-130">Valitse Näytä tulokset.</span><span class="sxs-lookup"><span data-stu-id="43f17-130">Click Show results.</span></span>
25. <span data-ttu-id="43f17-131">Avaa Tila-sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="43f17-131">Open Status column filter.</span></span>
26. <span data-ttu-id="43f17-132">Lajittele A–Z</span><span class="sxs-lookup"><span data-stu-id="43f17-132">Sort A to Z</span></span>

