---
title: Työehdotusten kehittäminen ja avaaminen
description: Työhönottoprojektit auttavat rekrytointiprosessissa.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20ee5d1bb624943d1ee67bbf2e7b5ecef1d59e9d
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693085"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="45b10-103">Työehdotusten kehittäminen ja avaaminen</span><span class="sxs-lookup"><span data-stu-id="45b10-103">Develop and open job requisition</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45b10-104">Työhönottoprojektit auttavat rekrytointiprosessissa.</span><span class="sxs-lookup"><span data-stu-id="45b10-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="45b10-105">Voit määrittää jokaiselle työhönottoprojektille tietoja, kuten työn, johon rekrytoidaan, rekrytoijan nimen, projektin tilan ja osaston, jossa työ sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="45b10-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="45b10-106">Kun työhönottoprojekti on luotu, voit kirjoittaa projektille työilmoituksen, julkaista sen työntekijöiden itsepalvelusivuilla, liittää työhakemukset projektiin ja seurata kyseisen projektin aktiviteetteja.</span><span class="sxs-lookup"><span data-stu-id="45b10-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="45b10-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="45b10-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="45b10-108">Aloita menettely valitse Henkilöstöhallinto > Työhönotto > Työhönottoprojektit > Työhönottoprojektit</span><span class="sxs-lookup"><span data-stu-id="45b10-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="45b10-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="45b10-109">Click New.</span></span>
2. <span data-ttu-id="45b10-110">Kirjoita arvo Työhönottoprojekti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45b10-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="45b10-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45b10-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="45b10-112">Avaa haku valitsemalla Rekrytoija-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45b10-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="45b10-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45b10-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="45b10-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45b10-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="45b10-115">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="45b10-115">Click Select.</span></span>
8. <span data-ttu-id="45b10-116">Avaa haku valitsemalla Osasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45b10-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="45b10-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45b10-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="45b10-118">Avaa haku valitsemalla Työ-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45b10-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="45b10-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45b10-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="45b10-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45b10-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="45b10-121">Syötä Avoimien paikkojen määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="45b10-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="45b10-122">Avaa haku valitsemalla Työhön ottava esimies -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45b10-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="45b10-123">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="45b10-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="45b10-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45b10-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="45b10-125">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="45b10-125">Click Select.</span></span>
18. <span data-ttu-id="45b10-126">Syötä päivämäärä Hakemuksen viimeinen jättöpäivä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="45b10-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="45b10-127">Valitse Media.</span><span class="sxs-lookup"><span data-stu-id="45b10-127">Click Media.</span></span>
    * <span data-ttu-id="45b10-128">Työhönottoprojektien avulla voidaan määrittää lehdistötiedotteita avointen työpaikkojen mainostamista varten.</span><span class="sxs-lookup"><span data-stu-id="45b10-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="45b10-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="45b10-129">Click New.</span></span>
21. <span data-ttu-id="45b10-130">Avaa haku valitsemalla Media-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="45b10-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="45b10-131">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="45b10-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="45b10-132">Syötä päivämäärä Aloituspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45b10-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="45b10-133">Syötä päivämäärä Päättymispäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="45b10-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="45b10-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="45b10-134">Click Save.</span></span>
26. <span data-ttu-id="45b10-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="45b10-135">Close the page.</span></span>
27. <span data-ttu-id="45b10-136">Valitse Työpaikkailmoitukset.</span><span class="sxs-lookup"><span data-stu-id="45b10-136">Click Job ads.</span></span>
28. <span data-ttu-id="45b10-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="45b10-137">Click Save.</span></span>
29. <span data-ttu-id="45b10-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="45b10-138">Close the page.</span></span>
30. <span data-ttu-id="45b10-139">Valitse Näytä työntekijän itsepalvelussa -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="45b10-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="45b10-140">Valitse Näytä työntekijän itsepalvelussa -valintaruutu, kun haluat työhönottoprojektin näkyvän työntekijöiden omilla itsepalvelusivuilla.</span><span class="sxs-lookup"><span data-stu-id="45b10-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="45b10-141">Valitse Työhönottoprojektin tila.</span><span class="sxs-lookup"><span data-stu-id="45b10-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="45b10-142">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="45b10-142">Click Start.</span></span>
    * <span data-ttu-id="45b10-143">Aloitettu tila tarkoittaa, että projekti on valmis vastaanottamaan hakemuksia.</span><span class="sxs-lookup"><span data-stu-id="45b10-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="45b10-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="45b10-144">Click OK.</span></span>

