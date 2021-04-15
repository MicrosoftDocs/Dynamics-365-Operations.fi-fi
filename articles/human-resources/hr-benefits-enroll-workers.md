---
title: Rekisteröi etuja työntekijöille ja poista niitä
description: Tässä menetelmässä käsitellään, miten yksittäiselle työtekijällä voidaan rekisteröidä vähintään yksi etu ja miten etu voidaan rekisteröidä usealle työntekijälle.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 47e8bf46d3d38cd1b776debb835d53a22e724149
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805847"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="7ff00-103">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="7ff00-103">Enroll and remove benefits from workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="7ff00-104">Tässä menetelmässä käsitellään, miten yksittäiselle työtekijällä voidaan rekisteröidä vähintään yksi etu ja miten etu voidaan rekisteröidä usealle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="7ff00-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="7ff00-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7ff00-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="7ff00-106">Rekisteröi edut yhdelle työntekijälle</span><span class="sxs-lookup"><span data-stu-id="7ff00-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="7ff00-107">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="7ff00-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="7ff00-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ff00-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7ff00-109">Valitse Edut.</span><span class="sxs-lookup"><span data-stu-id="7ff00-109">Click Benefits.</span></span>
4. <span data-ttu-id="7ff00-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7ff00-110">Click New.</span></span>
5. <span data-ttu-id="7ff00-111">Anna tai valitse Etu-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="7ff00-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="7ff00-112">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="7ff00-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="7ff00-113">Lisää Kattavuuden päättymispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="7ff00-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="7ff00-114">Laajenna Edunsaajat-osa, jos etuun on lisättävä edunsaajia.</span><span class="sxs-lookup"><span data-stu-id="7ff00-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="7ff00-115">Voit lisätä tältä sivulta tarvittaessa myös huollettavat.</span><span class="sxs-lookup"><span data-stu-id="7ff00-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="7ff00-116">Voit lisäksi muokata tällä sivulla edun rekisteröinnin tietoja tai poistaa rekisteröinnin.</span><span class="sxs-lookup"><span data-stu-id="7ff00-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="7ff00-117">Sulje sivu, kun edun rekisteröintiin tehtävät muutokset ovat valmiit.</span><span class="sxs-lookup"><span data-stu-id="7ff00-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="7ff00-118">Rekisteröi etu usealle työntekijälle</span><span class="sxs-lookup"><span data-stu-id="7ff00-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="7ff00-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ff00-119">Close the page.</span></span>
2. <span data-ttu-id="7ff00-120">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="7ff00-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="7ff00-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7ff00-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7ff00-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ff00-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7ff00-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7ff00-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7ff00-124">Valitse Rekisteröidy etuisuuksiin.</span><span class="sxs-lookup"><span data-stu-id="7ff00-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="7ff00-125">Anna tai valitse Etu-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="7ff00-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="7ff00-126">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="7ff00-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="7ff00-127">Lisää Kattavuuden päättymispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="7ff00-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="7ff00-128">Valitse Rekisteröi.</span><span class="sxs-lookup"><span data-stu-id="7ff00-128">Click Enroll.</span></span>
11. <span data-ttu-id="7ff00-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7ff00-129">Close the page.</span></span>
12. <span data-ttu-id="7ff00-130">Valitse Henkilöstöhallinto > Edut > Rekisteröityminen > Edun rekisteröinnin tulokset.</span><span class="sxs-lookup"><span data-stu-id="7ff00-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="7ff00-131">Etsi tarvitsemasi edun tulostietue.</span><span class="sxs-lookup"><span data-stu-id="7ff00-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="7ff00-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7ff00-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="7ff00-133">Voit tarkastella tällä sivulla, kenelle työntekijöille etu on rekisteröity ja kenelle ei.</span><span class="sxs-lookup"><span data-stu-id="7ff00-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]