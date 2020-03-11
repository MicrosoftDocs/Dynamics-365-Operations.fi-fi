---
title: Työsuhde-etuohjelman toteuttaminen
description: Tässä artikkelissa näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008950"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="f6c4a-103">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="f6c4a-103">Deliver employee benefits program</span></span>

<span data-ttu-id="f6c4a-104">Tässä artikkelissa näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="f6c4a-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f6c4a-106">Tämä tehtävä on tarkoitettu etuuspäällikölle.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="f6c4a-107">Edun elementtien luominen</span><span class="sxs-lookup"><span data-stu-id="f6c4a-107">Create benefit elements</span></span>
1. <span data-ttu-id="f6c4a-108">Tämä tehtävä alkaa Edut-luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="f6c4a-109">Aloita tehtävä avaamalla kyseinen sivu tai etsimällä Edut-luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="f6c4a-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-110">Click New.</span></span>
3. <span data-ttu-id="f6c4a-111">Syötä Tyyppi-kenttään luotavan edun tyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="f6c4a-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f6c4a-113">Valitse Samanaikainen rekisteröinti -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="f6c4a-114">Voit rajoittaa työntekijöiden mahdollisuutta rekisteröityä useisiin terveydenhoitosuunnitelmiin valitsemalla Yksi rekisteröinti tyyppiä kohti.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="f6c4a-115">Valitse Palkanlaskentaluokka-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="f6c4a-116">Valitse Suunnitelmat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="f6c4a-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-117">Click New.</span></span>
9. <span data-ttu-id="f6c4a-118">Kirjoita arvo Suunnitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="f6c4a-119">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f6c4a-120">Avaa haku valitsemalla Tyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f6c4a-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="f6c4a-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f6c4a-123">Valitse Palkanlaskennan vaikutus -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="f6c4a-124">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-124">Click the Options tab.</span></span>
16. <span data-ttu-id="f6c4a-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-125">Click New.</span></span>
17. <span data-ttu-id="f6c4a-126">Kirjoita arvo Asetus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="f6c4a-127">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="f6c4a-128">Edun luominen</span><span class="sxs-lookup"><span data-stu-id="f6c4a-128">Create a benefit</span></span>
1. <span data-ttu-id="f6c4a-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-129">Close the page.</span></span>
2. <span data-ttu-id="f6c4a-130">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="f6c4a-131">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="f6c4a-132">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f6c4a-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f6c4a-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f6c4a-135">Avaa haku valitsemalla Asetus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f6c4a-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f6c4a-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f6c4a-138">Syötä päivämäärä ja kellonaika Voimaantulo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="f6c4a-139">Valitse Uusi etu.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-139">Click Create benefit.</span></span>
12. <span data-ttu-id="f6c4a-140">Ota käyttöön Palkanlaskentatiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="f6c4a-141">Avaa haku valitsemalla Tiheys-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f6c4a-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f6c4a-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f6c4a-144">Valitse Peruste-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="f6c4a-145">Syötä Summa tai hinta -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f6c4a-145">In the Amount or rate field, enter a number.</span></span>
