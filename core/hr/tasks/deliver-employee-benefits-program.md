--- 
title: "Työsuhde-etuohjelman toteuttaminen"
description: "Tässä tehtävässä näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan."
author: kherr75
manager: AnnBe
ms.date: 12/01/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ec99b86d77c1381b4323a5faaea0487752eee9ed
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="deliver-an-employee-benefits-program"></a><span data-ttu-id="32263-103">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="32263-103">Deliver an employee benefits program</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32263-104">Tässä tehtävässä näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan.</span><span class="sxs-lookup"><span data-stu-id="32263-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="32263-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="32263-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="32263-106">Tämä tehtävä on tarkoitettu etuuspäällikölle.</span><span class="sxs-lookup"><span data-stu-id="32263-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="32263-107">Edun elementtien luominen</span><span class="sxs-lookup"><span data-stu-id="32263-107">Create benefit elements</span></span>
1. <span data-ttu-id="32263-108">Tämä tehtävä alkaa Edut-luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="32263-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="32263-109">Aloita tehtävä avaamalla kyseinen sivu tai etsimällä Edut-luettelosivu.</span><span class="sxs-lookup"><span data-stu-id="32263-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="32263-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="32263-110">Click New.</span></span>
3. <span data-ttu-id="32263-111">Syötä Tyyppi-kenttään luotavan edun tyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="32263-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="32263-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="32263-113">Valitse Samanaikainen rekisteröinti -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="32263-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="32263-114">Voit rajoittaa työntekijöiden mahdollisuutta rekisteröityä useisiin terveydenhoitosuunnitelmiin valitsemalla Yksi rekisteröinti tyyppiä kohti.</span><span class="sxs-lookup"><span data-stu-id="32263-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="32263-115">Valitse Palkanlaskentaluokka-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="32263-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="32263-116">Valitse Suunnitelmat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="32263-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="32263-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="32263-117">Click New.</span></span>
9. <span data-ttu-id="32263-118">Kirjoita arvo Suunnitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="32263-119">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="32263-120">Avaa haku valitsemalla Tyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="32263-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="32263-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="32263-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="32263-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="32263-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="32263-123">Valitse Palkanlaskennan vaikutus -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="32263-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="32263-124">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="32263-124">Click the Options tab.</span></span>
16. <span data-ttu-id="32263-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="32263-125">Click New.</span></span>
17. <span data-ttu-id="32263-126">Kirjoita arvo Asetus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="32263-127">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="32263-128">Edun luominen</span><span class="sxs-lookup"><span data-stu-id="32263-128">Create a benefit</span></span>
1. <span data-ttu-id="32263-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="32263-129">Close the page.</span></span>
2. <span data-ttu-id="32263-130">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="32263-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="32263-131">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="32263-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="32263-132">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="32263-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="32263-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="32263-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="32263-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="32263-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="32263-135">Avaa haku valitsemalla Asetus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="32263-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="32263-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="32263-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="32263-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="32263-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="32263-138">Syötä päivämäärä ja kellonaika Voimaantulo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="32263-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="32263-139">Valitse Uusi etu.</span><span class="sxs-lookup"><span data-stu-id="32263-139">Click Create benefit.</span></span>
12. <span data-ttu-id="32263-140">Ota käyttöön Palkanlaskentatiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="32263-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="32263-141">Avaa haku valitsemalla Tiheys-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="32263-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="32263-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="32263-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="32263-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="32263-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="32263-144">Valitse Peruste-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="32263-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="32263-145">Syötä Summa tai hinta -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="32263-145">In the Amount or rate field, enter a number.</span></span>


