---
title: Tehtäväsuhteen luonti – seuraaja
description: Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46dda12d4ad2b23ee86d240e6cdd8a1d46f1838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829231"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="17c03-103">Tehtäväsuhteen luonti – seuraaja</span><span class="sxs-lookup"><span data-stu-id="17c03-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17c03-104">Lean-tuotantovirran tehtävien työnkulku dokumentoidaan tehtäväsuhteiden kautta.</span><span class="sxs-lookup"><span data-stu-id="17c03-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="17c03-105">Tässä tallenteessa käsitellään tehtäväsuhteen luontia.</span><span class="sxs-lookup"><span data-stu-id="17c03-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="17c03-106">Edellytykset:</span><span class="sxs-lookup"><span data-stu-id="17c03-106">Prerequisites:</span></span>

- <span data-ttu-id="17c03-107">Tuotantovirta ja versio luonnostilassa.</span><span class="sxs-lookup"><span data-stu-id="17c03-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="17c03-108">Tuotantovirtaan luodaan kaksi toisiaan seuraavaa tehtävää, jotka eivät ole suhteessa toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="17c03-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="17c03-109">Etsi tuotantovirran versio</span><span class="sxs-lookup"><span data-stu-id="17c03-109">Find the production flow version</span></span> 
1. <span data-ttu-id="17c03-110">Valitse Tuotannonhallinta > Asetukset > Lean-tuotantovirta > Tuotantovirrat.</span><span class="sxs-lookup"><span data-stu-id="17c03-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="17c03-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="17c03-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="17c03-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="17c03-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="17c03-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="17c03-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="17c03-114">Valitse luonnosversio luettelosta.</span><span class="sxs-lookup"><span data-stu-id="17c03-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="17c03-115">Tehtäväsuhteet voidaan lisätä sekä tuotantovirran luonnosversioihin että aktiivisiin versioihin.</span><span class="sxs-lookup"><span data-stu-id="17c03-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="17c03-116">Avaa tehtävän yhteenveto</span><span class="sxs-lookup"><span data-stu-id="17c03-116">Open the activity overview</span></span>
1. <span data-ttu-id="17c03-117">Valitse Tehtävät.</span><span class="sxs-lookup"><span data-stu-id="17c03-117">Click Activities.</span></span>
    * <span data-ttu-id="17c03-118">Huomaa, että lomake näyttää kaikki tuotantovirran tehtävät, jotka on kohdistettu siihen tuotantovirtojen versioon, jossa työskentelet.</span><span class="sxs-lookup"><span data-stu-id="17c03-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="17c03-119">Lisää seuraaja</span><span class="sxs-lookup"><span data-stu-id="17c03-119">Add a Successor</span></span>
1. <span data-ttu-id="17c03-120">Valitse Lisää seuraaja.</span><span class="sxs-lookup"><span data-stu-id="17c03-120">Click Add successor.</span></span>
2. <span data-ttu-id="17c03-121">Avaa haku napsauttamalla Tehtävä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="17c03-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="17c03-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="17c03-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="17c03-123">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="17c03-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="17c03-124">Valitse Rajoitus-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="17c03-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="17c03-125">Lisää Rajoitusarvo-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="17c03-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="17c03-126">Aikarajoitus on edeltäjän (eräpäivä ja -aika) ajoitetun lopun ja seuraajan ajoitetun alun väliin ajoitettava aika.</span><span class="sxs-lookup"><span data-stu-id="17c03-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="17c03-127">Kirjoita Yksiköt-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="17c03-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="17c03-128">Lisää Syklin kestojen suhde -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="17c03-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="17c03-129">Jos molemmat tehtävät suoritetaan samassa tahdissa, syklin keston suhteen on oltava 1.</span><span class="sxs-lookup"><span data-stu-id="17c03-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="17c03-130">Jos edeltäjä suoritetaan seuraajan kaksinkertaisella tahdilla, suhteen on oltava 2.</span><span class="sxs-lookup"><span data-stu-id="17c03-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="17c03-131">Syklin kestosuhteita käytetään tuotantovirtatehtävien yksittäisten syklien kestojen laskentaan.</span><span class="sxs-lookup"><span data-stu-id="17c03-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="17c03-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="17c03-132">Click OK.</span></span>
10. <span data-ttu-id="17c03-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="17c03-133">Close the page.</span></span>
11. <span data-ttu-id="17c03-134">Valitse Ruudukkoruutu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="17c03-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="17c03-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="17c03-135">Close the page.</span></span>
13. <span data-ttu-id="17c03-136">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="17c03-136">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]