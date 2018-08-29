--- 
title: "Joukkotyöhönottoprojektien luominen"
description: "Tässä menettelyssä esitellään joukkotyöhönottoprojektin määritysprosessi."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 7059ad6cc438473111e9a6116a4e6fadc7016904
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="create-mass-hire-projects"></a><span data-ttu-id="b8042-103">Joukkotyöhönottoprojektien luominen</span><span class="sxs-lookup"><span data-stu-id="b8042-103">Create mass hire projects</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8042-104">Tässä menettelyssä esitellään joukkotyöhönottoprojektin määritysprosessi.</span><span class="sxs-lookup"><span data-stu-id="b8042-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="b8042-105">Rekrytoija voi luoda useita toimia ja palkata useita työntekijöitä näihin toimiin joukkotyöhönottoprojektien avulla.</span><span class="sxs-lookup"><span data-stu-id="b8042-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="b8042-106">Aloita tämä menettely siirtymällä kohtaan Henkilöstöhallinto > Työhönotto > Joukkotyöhönottoprojektit.</span><span class="sxs-lookup"><span data-stu-id="b8042-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="b8042-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b8042-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b8042-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8042-108">Click New.</span></span>
2. <span data-ttu-id="b8042-109">Syötä arvo Joukkotyöhönottoprojekti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8042-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="b8042-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8042-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="b8042-111">Syötä Projektin alku -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b8042-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="b8042-112">Syötä Projektin loppu -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b8042-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="b8042-113">Valitse Avaa projekti.</span><span class="sxs-lookup"><span data-stu-id="b8042-113">Click Open project.</span></span>
7. <span data-ttu-id="b8042-114">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b8042-114">Click Yes.</span></span>
8. <span data-ttu-id="b8042-115">Valitse Luo toimia.</span><span class="sxs-lookup"><span data-stu-id="b8042-115">Click Create positions.</span></span>
9. <span data-ttu-id="b8042-116">Syötä Määrä-kenttään luotavien toimien määrä.</span><span class="sxs-lookup"><span data-stu-id="b8042-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="b8042-117">Aloituspäivämäärästä tulee uusien työntekijöiden työhönottopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b8042-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="b8042-118">Päätymispäivämäärästä tulee uusien työntekijöiden työsuhteen loppumispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b8042-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="b8042-119">Määritä, ovatko uudet työntekijät työntekijöitä vai alihankkijoita.</span><span class="sxs-lookup"><span data-stu-id="b8042-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="b8042-120">Valitse avattavan valikon painike ja valitse Työ-kentässä työ, jolle toimet luodaan.</span><span class="sxs-lookup"><span data-stu-id="b8042-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="b8042-121">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b8042-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b8042-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b8042-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b8042-123">Kokopäiväisten työntekijöiden oletusarvo saadaan valitusta työstä.</span><span class="sxs-lookup"><span data-stu-id="b8042-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="b8042-124">Arvoa voi muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="b8042-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="b8042-125">Vaihtoehtoisesti voit valita uusille toimille osaston.</span><span class="sxs-lookup"><span data-stu-id="b8042-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="b8042-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b8042-126">Click OK.</span></span>


