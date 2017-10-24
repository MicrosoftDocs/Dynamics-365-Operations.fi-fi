--- 
title: Rajoitetun suunnitelman luominen
description: "Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="e48de-103">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="e48de-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e48de-104">Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.</span><span class="sxs-lookup"><span data-stu-id="e48de-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="e48de-105">Suunnitelma varmistaa, että valmistus aloitetaan vasta sitten, kun materiaalit ovat käytettävissä. Se myös estää resurssien ylivaraamisen.</span><span class="sxs-lookup"><span data-stu-id="e48de-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="e48de-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="e48de-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e48de-107">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="e48de-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="e48de-108">Rajoitetun suunnitelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e48de-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="e48de-109">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="e48de-109">Click Master planning.</span></span>
2. <span data-ttu-id="e48de-110">Valitse Pääsuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="e48de-110">Click Master plans.</span></span>
3. <span data-ttu-id="e48de-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e48de-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e48de-112">Esimerkki: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="e48de-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="e48de-113">Valitse Rajallinen kapasiteetti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="e48de-114">Syötä Rajallisen kapasiteetin aikaraja -kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="e48de-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="e48de-115">Laajenna Päivät-osan aikarajat.</span><span class="sxs-lookup"><span data-stu-id="e48de-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="e48de-116">Valitse Kapasiteetti-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="e48de-117">Syötä Kapasiteetin aikataulutuksen aikaraja (päivää) -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e48de-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="e48de-118">Esimerkki: 60</span><span class="sxs-lookup"><span data-stu-id="e48de-118">Example: 60</span></span>  
9. <span data-ttu-id="e48de-119">Valitse Lasketut viiveet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="e48de-120">Syötä Laskettujen viiveiden aikaraja (päivää) -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e48de-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="e48de-121">Esimerkki: 60</span><span class="sxs-lookup"><span data-stu-id="e48de-121">Example: 60</span></span>  
11. <span data-ttu-id="e48de-122">Laajenna Lasketut viiveet -osa.</span><span class="sxs-lookup"><span data-stu-id="e48de-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="e48de-123">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="e48de-124">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="e48de-125">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="e48de-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="e48de-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e48de-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="e48de-127">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="e48de-127">Create a constrained plan</span></span>
1. <span data-ttu-id="e48de-128">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="e48de-128">Click Run.</span></span>
2. <span data-ttu-id="e48de-129">Syötä tai valitse arvo Pääsuunnitelma-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e48de-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="e48de-130">Valitse suunnitelma, jolle määritit rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="e48de-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="e48de-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e48de-131">Click OK.</span></span>
    * <span data-ttu-id="e48de-132">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="e48de-132">This may take a while.</span></span>  
4. <span data-ttu-id="e48de-133">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="e48de-133">Click Planned orders.</span></span>


