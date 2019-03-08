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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2019
ms.locfileid: "352456"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="a9996-103">Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla</span><span class="sxs-lookup"><span data-stu-id="a9996-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9996-104">Menettely keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.</span><span class="sxs-lookup"><span data-stu-id="a9996-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="a9996-105">Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella.</span><span class="sxs-lookup"><span data-stu-id="a9996-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="a9996-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a9996-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="a9996-107">Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.</span><span class="sxs-lookup"><span data-stu-id="a9996-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="a9996-108">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="a9996-108">Create a production order</span></span>
1. <span data-ttu-id="a9996-109">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="a9996-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="a9996-110">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="a9996-110">Click New production order.</span></span>
3. <span data-ttu-id="a9996-111">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a9996-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a9996-112">Valitse nimiketunnus D0001.</span><span class="sxs-lookup"><span data-stu-id="a9996-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="a9996-113">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="a9996-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="a9996-114">Ajoita tuotantotilauksen työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="a9996-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="a9996-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a9996-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a9996-116">Valitse juuri luomasi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="a9996-116">Select the production order that you have just created.</span></span> <span data-ttu-id="a9996-117">Sen pitäisi olla ensimmäisenä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a9996-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="a9996-118">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="a9996-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="a9996-119">Valitse Ajoita työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="a9996-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="a9996-120">Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a9996-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="a9996-121">Anna Ajoituspäivämäärä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a9996-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="a9996-122">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="a9996-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="a9996-123">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a9996-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="a9996-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a9996-124">Click OK.</span></span>
7. <span data-ttu-id="a9996-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a9996-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a9996-126">Huomaa, että tila on nyt Ajoitettu.</span><span class="sxs-lookup"><span data-stu-id="a9996-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="a9996-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a9996-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a9996-128">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="a9996-128">Click All jobs.</span></span>
    * <span data-ttu-id="a9996-129">Huomaa, että työvaiheiden ajoituksella ei luoda töitä.</span><span class="sxs-lookup"><span data-stu-id="a9996-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="a9996-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a9996-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="a9996-131">Ajoita tuotantotilauksen työt.</span><span class="sxs-lookup"><span data-stu-id="a9996-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="a9996-132">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="a9996-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="a9996-133">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="a9996-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="a9996-134">Valitse Ajoituksen suunta -kentässä Ajoituspäivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a9996-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="a9996-135">Anna Ajoituspäivämäärä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a9996-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="a9996-136">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="a9996-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="a9996-137">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a9996-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="a9996-138">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a9996-138">Click OK.</span></span>
6. <span data-ttu-id="a9996-139">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="a9996-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="a9996-140">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="a9996-140">Click All jobs.</span></span>
    * <span data-ttu-id="a9996-141">Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.</span><span class="sxs-lookup"><span data-stu-id="a9996-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

