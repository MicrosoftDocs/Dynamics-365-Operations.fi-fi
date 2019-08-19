---
title: Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla
description: Menettely keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4932cfa472c34a16249b226aa4a07b8e5f528053
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838484"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="31d17-103">Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla</span><span class="sxs-lookup"><span data-stu-id="31d17-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31d17-104">Menettely keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.</span><span class="sxs-lookup"><span data-stu-id="31d17-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="31d17-105">Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella.</span><span class="sxs-lookup"><span data-stu-id="31d17-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="31d17-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="31d17-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="31d17-107">Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.</span><span class="sxs-lookup"><span data-stu-id="31d17-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="31d17-108">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="31d17-108">Create a production order</span></span>
1. <span data-ttu-id="31d17-109">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="31d17-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="31d17-110">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="31d17-110">Click New production order.</span></span>
3. <span data-ttu-id="31d17-111">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="31d17-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="31d17-112">Valitse nimiketunnus D0001.</span><span class="sxs-lookup"><span data-stu-id="31d17-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="31d17-113">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="31d17-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="31d17-114">Ajoita tuotantotilauksen työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="31d17-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="31d17-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="31d17-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="31d17-116">Valitse juuri luomasi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="31d17-116">Select the production order that you have just created.</span></span> <span data-ttu-id="31d17-117">Sen pitäisi olla ensimmäisenä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="31d17-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="31d17-118">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="31d17-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="31d17-119">Valitse Ajoita työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="31d17-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="31d17-120">Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="31d17-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="31d17-121">Anna Ajoituspäivämäärä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="31d17-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="31d17-122">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="31d17-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="31d17-123">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="31d17-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="31d17-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31d17-124">Click OK.</span></span>
7. <span data-ttu-id="31d17-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="31d17-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="31d17-126">Huomaa, että tila on nyt Ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="31d17-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="31d17-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="31d17-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="31d17-128">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="31d17-128">Click All jobs.</span></span>
    * <span data-ttu-id="31d17-129">Huomaa, että työvaiheiden ajoituksella ei luoda töitä.</span><span class="sxs-lookup"><span data-stu-id="31d17-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="31d17-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="31d17-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="31d17-131">Ajoita tuotantotilauksen työt.</span><span class="sxs-lookup"><span data-stu-id="31d17-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="31d17-132">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="31d17-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="31d17-133">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="31d17-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="31d17-134">Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="31d17-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="31d17-135">Anna Ajoituspäivämäärä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="31d17-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="31d17-136">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="31d17-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="31d17-137">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="31d17-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="31d17-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="31d17-138">Click OK.</span></span>
6. <span data-ttu-id="31d17-139">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="31d17-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="31d17-140">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="31d17-140">Click All jobs.</span></span>
    * <span data-ttu-id="31d17-141">Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.</span><span class="sxs-lookup"><span data-stu-id="31d17-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

