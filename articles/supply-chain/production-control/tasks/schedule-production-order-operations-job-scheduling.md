---
title: Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla
description: Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a69339bc678de8343dbf2646a4d6fe0ace9964c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210476"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="39955-103">Ajoita tuotantotilaus työvaiheiden ja töiden ajoittamisen avulla</span><span class="sxs-lookup"><span data-stu-id="39955-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39955-104">Tämä aihe keskittyy tuotantotilaukseen ajoittamiseen työvaiheiden ja töiden ajoittamisella.</span><span class="sxs-lookup"><span data-stu-id="39955-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="39955-105">Vaikka yhtään työtä ei luotu työvaiheiden ajoituksella, töitä luotiin töiden ajoituksella.</span><span class="sxs-lookup"><span data-stu-id="39955-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="39955-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="39955-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="39955-107">Tämä menettely on tarkoitettu erillisessä valmistusympäristössä työskentelevälle tuotantopäällikölle, tuotantosuunnittelijalle tai työnohjauksen valvojalle.</span><span class="sxs-lookup"><span data-stu-id="39955-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="39955-108">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="39955-108">Create a production order</span></span>
1. <span data-ttu-id="39955-109">Valitse siirtymisruudussa **Moduulit >Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="39955-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="39955-110">Valitse **Uusi tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="39955-110">Select **New production order**.</span></span>
3. <span data-ttu-id="39955-111">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="39955-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="39955-112">Valitse nimiketunnus **D0001**.</span><span class="sxs-lookup"><span data-stu-id="39955-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="39955-113">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="39955-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="39955-114">Ajoita tuotantotilauksen työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="39955-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="39955-115">Merkitse juuri luotu rivi.</span><span class="sxs-lookup"><span data-stu-id="39955-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="39955-116">Valitse toimintoruudussa **Ajoitus**.</span><span class="sxs-lookup"><span data-stu-id="39955-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="39955-117">Valitse **Ajoita työvaiheet**.</span><span class="sxs-lookup"><span data-stu-id="39955-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="39955-118">Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="39955-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="39955-119">Anna **Ajoituspäivämäärä**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="39955-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="39955-120">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="39955-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="39955-121">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="39955-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="39955-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="39955-122">Select **OK**.</span></span>
7. <span data-ttu-id="39955-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="39955-123">In the list, mark the selected row.</span></span> <span data-ttu-id="39955-124">Huomaa, että tila on nyt **Ajoitettu**.</span><span class="sxs-lookup"><span data-stu-id="39955-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="39955-125">Valitset **Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="39955-125">Select **All jobs**.</span></span> <span data-ttu-id="39955-126">Huomaa, että työvaiheiden ajoituksella ei luoda töitä.</span><span class="sxs-lookup"><span data-stu-id="39955-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="39955-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="39955-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="39955-128">Ajoita tuotantotilauksen työt.</span><span class="sxs-lookup"><span data-stu-id="39955-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="39955-129">Valitse toimintoruudussa **Ajoitus**.</span><span class="sxs-lookup"><span data-stu-id="39955-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="39955-130">Valitse **Ajoita työt**.</span><span class="sxs-lookup"><span data-stu-id="39955-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="39955-131">Valitse **Ajoituksen suunta** -kentässä **Ajoituspäivästä eteenpäin**.</span><span class="sxs-lookup"><span data-stu-id="39955-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="39955-132">Anna **Ajoituspäivämäärä**-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="39955-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="39955-133">Valitse tuleva päivämäärä, kuten tämä päivä viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="39955-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="39955-134">Valitulla ajoituksen suunnalla tuotantotilaus ajoitetaan tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="39955-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="39955-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="39955-135">Select **OK**.</span></span>
6. <span data-ttu-id="39955-136">Valitse toimintoruudussa **Tuotantotilaus**.</span><span class="sxs-lookup"><span data-stu-id="39955-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="39955-137">Valitset **Kaikki työt**.</span><span class="sxs-lookup"><span data-stu-id="39955-137">Select **All jobs**.</span></span> <span data-ttu-id="39955-138">Huomaa, että aktiivisen reitin perusteella töiden ajoituksella luontiin viisi työtä.</span><span class="sxs-lookup"><span data-stu-id="39955-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

