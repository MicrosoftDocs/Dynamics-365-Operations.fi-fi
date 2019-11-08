---
title: Tehtäväsuhteen luonti – seuraaja
description: Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07ebb7d2158964a5d8862df998fe470032a0d354
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550410"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="7927a-103">Tehtäväsuhteen luonti – seuraaja</span><span class="sxs-lookup"><span data-stu-id="7927a-103">Create activity relation - Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7927a-104">Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.</span><span class="sxs-lookup"><span data-stu-id="7927a-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="7927a-105">Tässä tallenteessa käsitellään tehtäväsuhteen luontia.</span><span class="sxs-lookup"><span data-stu-id="7927a-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="7927a-106">Edellytykset:</span><span class="sxs-lookup"><span data-stu-id="7927a-106">Prerequisites:</span></span>

- <span data-ttu-id="7927a-107">Tuotantovirta ja versio luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="7927a-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="7927a-108">Tuotantovirtaan luodaan kaksi toisiaan seuraavaa tehtävää, jotka eivät ole suhteessa toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="7927a-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="7927a-109">Etsi tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="7927a-109">Find the production flow version</span></span> 
1. <span data-ttu-id="7927a-110">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="7927a-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="7927a-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7927a-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7927a-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7927a-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7927a-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="7927a-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="7927a-114">Valitse luonnosversio luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7927a-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="7927a-115">Tehtäväsuhteet voidaan lisätä sekä tuotantovirran luonnosversioihin että aktiivisiin versioihin.</span><span class="sxs-lookup"><span data-stu-id="7927a-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="7927a-116">Avaa tehtävän yhteenveto</span><span class="sxs-lookup"><span data-stu-id="7927a-116">Open the activity overview</span></span>
1. <span data-ttu-id="7927a-117">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7927a-117">Click Activities.</span></span>
    * <span data-ttu-id="7927a-118">Huomaa, että lomake näyttää kaikki tuotantovirran tehtävät, jotka on kohdistettu siihen tuotantovirtojen versioon, jossa työskentelet.</span><span class="sxs-lookup"><span data-stu-id="7927a-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="7927a-119">Lisää seuraaja</span><span class="sxs-lookup"><span data-stu-id="7927a-119">Add a Successor</span></span>
1. <span data-ttu-id="7927a-120">Valitse Lisää seuraaja.</span><span class="sxs-lookup"><span data-stu-id="7927a-120">Click Add successor.</span></span>
2. <span data-ttu-id="7927a-121">Avaa haku napsauttamalla Tehtävä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="7927a-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7927a-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7927a-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7927a-123">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7927a-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7927a-124">Valitse Rajoitus-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7927a-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="7927a-125">Lisää Rajoitusarvo-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7927a-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="7927a-126">Aikarajoitus on edeltäjän (eräpäivä ja -aika) ajoitetun lopun ja seuraajan ajoitetun alun väliin ajoitettava aika.</span><span class="sxs-lookup"><span data-stu-id="7927a-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="7927a-127">Kirjoita Yksiköt-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7927a-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="7927a-128">Lisää Syklin kestojen suhde -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7927a-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="7927a-129">Jos molemmat tehtävät suoritetaan samassa tahdissa, syklin keston suhteen on oltava 1.</span><span class="sxs-lookup"><span data-stu-id="7927a-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="7927a-130">Jos edeltäjä suoritetaan seuraajan kaksinkertaisella tahdilla, suhteen on oltava 2.</span><span class="sxs-lookup"><span data-stu-id="7927a-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="7927a-131">Syklin kestosuhteita käytetään tuotantovirtatehtävien yksittäisten syklien kestojen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="7927a-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="7927a-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7927a-132">Click OK.</span></span>
10. <span data-ttu-id="7927a-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7927a-133">Close the page.</span></span>
11. <span data-ttu-id="7927a-134">Valitse Ruudukkoruutu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7927a-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="7927a-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7927a-135">Close the page.</span></span>
13. <span data-ttu-id="7927a-136">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="7927a-136">Refresh the page.</span></span>

