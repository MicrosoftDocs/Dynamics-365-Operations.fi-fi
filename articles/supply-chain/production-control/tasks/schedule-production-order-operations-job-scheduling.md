---
title: Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla
description: Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841380"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="07b32-103">Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla</span><span class="sxs-lookup"><span data-stu-id="07b32-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07b32-104">Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.</span><span class="sxs-lookup"><span data-stu-id="07b32-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="07b32-105">Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella.</span><span class="sxs-lookup"><span data-stu-id="07b32-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="07b32-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="07b32-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="07b32-107">Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.</span><span class="sxs-lookup"><span data-stu-id="07b32-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="07b32-108">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="07b32-108">Create a production order</span></span>
1. <span data-ttu-id="07b32-109">Valitse siirtymisruudussa **Moduulit >Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="07b32-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="07b32-110">Valitse **Uusi tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="07b32-110">Select **New production order**.</span></span>
3. <span data-ttu-id="07b32-111">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="07b32-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="07b32-112">Valitse nimiketunnus **D0001**.</span><span class="sxs-lookup"><span data-stu-id="07b32-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="07b32-113">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="07b32-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="07b32-114">Ajoita tuotantotilauksen työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="07b32-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="07b32-115">Merkitse juuri luotu rivi.</span><span class="sxs-lookup"><span data-stu-id="07b32-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="07b32-116">Valitse toimintoruudussa **Ajoitus**.</span><span class="sxs-lookup"><span data-stu-id="07b32-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="07b32-117">Valitse **Ajoita työvaiheet**.</span><span class="sxs-lookup"><span data-stu-id="07b32-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="07b32-118">Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="07b32-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="07b32-119">Anna **Ajoituspäivämäärä**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="07b32-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="07b32-120">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="07b32-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="07b32-121">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="07b32-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="07b32-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="07b32-122">Select **OK**.</span></span>
7. <span data-ttu-id="07b32-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="07b32-123">In the list, mark the selected row.</span></span> <span data-ttu-id="07b32-124">Huomaa, että tila on nyt **Ajoitettu**.</span><span class="sxs-lookup"><span data-stu-id="07b32-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="07b32-125">Valitset **Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="07b32-125">Select **All jobs**.</span></span> <span data-ttu-id="07b32-126">Huomaa, että työvaiheiden ajoituksella ei luoda töitä.</span><span class="sxs-lookup"><span data-stu-id="07b32-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="07b32-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="07b32-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="07b32-128">Ajoita tuotantotilauksen työt.</span><span class="sxs-lookup"><span data-stu-id="07b32-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="07b32-129">Valitse toimintoruudussa **Ajoitus**.</span><span class="sxs-lookup"><span data-stu-id="07b32-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="07b32-130">Valitse **Ajoita työt**.</span><span class="sxs-lookup"><span data-stu-id="07b32-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="07b32-131">Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="07b32-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="07b32-132">Anna **Ajoituspäivämäärä**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="07b32-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="07b32-133">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="07b32-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="07b32-134">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="07b32-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="07b32-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="07b32-135">Select **OK**.</span></span>
6. <span data-ttu-id="07b32-136">Valitse toimintoruudussa **Tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="07b32-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="07b32-137">Valitset **Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="07b32-137">Select **All jobs**.</span></span> <span data-ttu-id="07b32-138">Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.</span><span class="sxs-lookup"><span data-stu-id="07b32-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]