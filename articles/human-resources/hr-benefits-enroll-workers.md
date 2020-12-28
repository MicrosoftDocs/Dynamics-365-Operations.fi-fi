---
title: Rekisteröi etuja työntekijöille ja poista niitä
description: Tässä menetelmässä käsitellään, miten yksittäiselle työtekijällä voidaan rekisteröidä vähintään yksi etu ja miten etu voidaan rekisteröidä usealle työntekijälle.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 36fd724ff27cbb646f3f8a35ca1b30dc86a5afe4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418246"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="d9a3d-103">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="d9a3d-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="d9a3d-104">Tässä menetelmässä käsitellään, miten yksittäiselle työtekijällä voidaan rekisteröidä vähintään yksi etu ja miten etu voidaan rekisteröidä usealle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="d9a3d-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="d9a3d-106">Rekisteröi edut yhdelle työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d9a3d-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="d9a3d-107">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="d9a3d-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d9a3d-109">Valitse Edut.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-109">Click Benefits.</span></span>
4. <span data-ttu-id="d9a3d-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-110">Click New.</span></span>
5. <span data-ttu-id="d9a3d-111">Anna tai valitse Etu-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="d9a3d-112">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="d9a3d-113">Lisää Kattavuuden päättymispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="d9a3d-114">Laajenna Edunsaajat-osa, jos etuun on lisättävä edunsaajia.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="d9a3d-115">Voit lisätä tältä sivulta tarvittaessa myös huollettavat.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="d9a3d-116">Voit lisäksi muokata tällä sivulla edun rekisteröinnin tietoja tai poistaa rekisteröinnin.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="d9a3d-117">Sulje sivu, kun edun rekisteröintiin tehtävät muutokset ovat valmiit.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="d9a3d-118">Rekisteröi etu usealle työntekijälle</span><span class="sxs-lookup"><span data-stu-id="d9a3d-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="d9a3d-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-119">Close the page.</span></span>
2. <span data-ttu-id="d9a3d-120">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="d9a3d-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d9a3d-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d9a3d-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d9a3d-124">Valitse Rekisteröidy etuisuuksiin.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="d9a3d-125">Anna tai valitse Etu-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="d9a3d-126">Lisää Kattavuuden alkamispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="d9a3d-127">Lisää Kattavuuden päättymispäivämäärä -kenttään päivämäärä ja kellonaika.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="d9a3d-128">Valitse Rekisteröi.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-128">Click Enroll.</span></span>
11. <span data-ttu-id="d9a3d-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-129">Close the page.</span></span>
12. <span data-ttu-id="d9a3d-130">Valitse Henkilöstöhallinto > Edut > Rekisteröityminen > Edun rekisteröinnin tulokset.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="d9a3d-131">Etsi tarvitsemasi edun tulostietue.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="d9a3d-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d9a3d-133">Voit tarkastella tällä sivulla, kenelle työntekijöille etu on rekisteröity ja kenelle ei.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

