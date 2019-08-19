---
title: Rajoitetun suunnitelman luominen
description: Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845287"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="54df0-103">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="54df0-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54df0-104">Tässä menettelyssä kerrotaan, miten luodaan suunnitelma, jossa huomioidaan sekä kapasiteetti- ja materiaalirajoitukset.</span><span class="sxs-lookup"><span data-stu-id="54df0-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="54df0-105">Suunnitelma varmistaa, että valmistus aloitetaan vasta sitten, kun materiaalit ovat käytettävissä. Se myös estää resurssien ylivaraamisen.</span><span class="sxs-lookup"><span data-stu-id="54df0-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="54df0-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="54df0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="54df0-107">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="54df0-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="54df0-108">Rajoitetun suunnitelman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="54df0-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="54df0-109">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="54df0-109">Click Master planning.</span></span>
2. <span data-ttu-id="54df0-110">Valitse Pääsuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="54df0-110">Click Master plans.</span></span>
3. <span data-ttu-id="54df0-111">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="54df0-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54df0-112">Esimerkki: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="54df0-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="54df0-113">Valitse Rajallinen kapasiteetti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="54df0-114">Syötä Rajallisen kapasiteetin aikaraja -kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="54df0-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="54df0-115">Laajenna Päivät-osan aikarajat.</span><span class="sxs-lookup"><span data-stu-id="54df0-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="54df0-116">Valitse Kapasiteetti-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="54df0-117">Syötä Kapasiteetin aikataulutuksen aikaraja (päivää) -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="54df0-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="54df0-118">Esimerkki: 60</span><span class="sxs-lookup"><span data-stu-id="54df0-118">Example: 60</span></span>  
9. <span data-ttu-id="54df0-119">Valitse Lasketut viiveet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="54df0-120">Syötä Laskettujen viiveiden aikaraja (päivää) -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="54df0-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="54df0-121">Esimerkki: 60</span><span class="sxs-lookup"><span data-stu-id="54df0-121">Example: 60</span></span>  
11. <span data-ttu-id="54df0-122">Laajenna Lasketut viiveet -osa.</span><span class="sxs-lookup"><span data-stu-id="54df0-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="54df0-123">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="54df0-124">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="54df0-125">Valitse Lisää laskettu viive tarvepäivämäärään -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="54df0-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="54df0-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="54df0-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="54df0-127">Rajoitetun suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="54df0-127">Create a constrained plan</span></span>
1. <span data-ttu-id="54df0-128">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="54df0-128">Click Run.</span></span>
2. <span data-ttu-id="54df0-129">Syötä tai valitse arvo Pääsuunnitelma-kentässä.</span><span class="sxs-lookup"><span data-stu-id="54df0-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="54df0-130">Valitse suunnitelma, jolle määritit rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="54df0-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="54df0-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="54df0-131">Click OK.</span></span>
    * <span data-ttu-id="54df0-132">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="54df0-132">This may take a while.</span></span>  
4. <span data-ttu-id="54df0-133">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="54df0-133">Click Planned orders.</span></span>

