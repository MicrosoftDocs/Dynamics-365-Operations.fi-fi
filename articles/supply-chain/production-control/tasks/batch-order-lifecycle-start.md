---
title: Erän tilauksen elinkaari luomisesta käynnistämiseen
description: Tämä menettely käsittelee erätilauksen elinkaaren ensimmäistä osaa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a1803822bebf58a3370afe8c5dc9f519c65917d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843814"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="0fa89-103">Erän tilauksen elinkaari luomisesta käynnistämiseen</span><span class="sxs-lookup"><span data-stu-id="0fa89-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0fa89-104">Tämä menettely käsittelee erätilauksen elinkaaren ensimmäistä osaa.</span><span class="sxs-lookup"><span data-stu-id="0fa89-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="0fa89-105">Luonnista, kustannusten arvioinnista ja ylituotantotyön ajoittamisesta erätilauksen todelliseen aloittamiseen.</span><span class="sxs-lookup"><span data-stu-id="0fa89-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="0fa89-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="0fa89-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="0fa89-107">Jos menetelmä suoritetaan toisella tietojoukolla, edellytyksenä on, että vapautetussa tuotteessa on aktiviinen resepti- ja reittiversio.</span><span class="sxs-lookup"><span data-stu-id="0fa89-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="0fa89-108">Erätilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="0fa89-108">Create a batch order</span></span>
1. <span data-ttu-id="0fa89-109">Valitse Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="0fa89-109">Go to All production orders.</span></span>
2. <span data-ttu-id="0fa89-110">Valitse Uusi erätilaus.</span><span class="sxs-lookup"><span data-stu-id="0fa89-110">Click New batch order.</span></span>
3. <span data-ttu-id="0fa89-111">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0fa89-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="0fa89-112">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="0fa89-112">Click Create.</span></span>
5. <span data-ttu-id="0fa89-113">Suodata pikasuodattimella Tuotanto-kenttää arvolla b.</span><span class="sxs-lookup"><span data-stu-id="0fa89-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="0fa89-114">Näytä tuotantoresepti ja odotetut oheistuotteet</span><span class="sxs-lookup"><span data-stu-id="0fa89-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="0fa89-115">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="0fa89-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="0fa89-116">Valitse Resepti.</span><span class="sxs-lookup"><span data-stu-id="0fa89-116">Click Formula.</span></span>
3. <span data-ttu-id="0fa89-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-117">Close the page.</span></span>
4. <span data-ttu-id="0fa89-118">Valitse Oheistuotteet.</span><span class="sxs-lookup"><span data-stu-id="0fa89-118">Click Co-products.</span></span>
5. <span data-ttu-id="0fa89-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="0fa89-120">Arvioi erätilaus</span><span class="sxs-lookup"><span data-stu-id="0fa89-120">Estimate the batch order</span></span>
1. <span data-ttu-id="0fa89-121">Valitse Arvio.</span><span class="sxs-lookup"><span data-stu-id="0fa89-121">Click Estimate.</span></span>
2. <span data-ttu-id="0fa89-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0fa89-122">Click OK.</span></span>
3. <span data-ttu-id="0fa89-123">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="0fa89-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="0fa89-124">Valitse Näytä laskennan tiedot.</span><span class="sxs-lookup"><span data-stu-id="0fa89-124">Click View calculation details.</span></span>
5. <span data-ttu-id="0fa89-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="0fa89-126">Vapauta erätilaus</span><span class="sxs-lookup"><span data-stu-id="0fa89-126">Release the batch order</span></span>
1. <span data-ttu-id="0fa89-127">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="0fa89-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="0fa89-128">Valitse Vapauta.</span><span class="sxs-lookup"><span data-stu-id="0fa89-128">Click Release.</span></span>
3. <span data-ttu-id="0fa89-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0fa89-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="0fa89-130">Ajoita tuotantotyöt</span><span class="sxs-lookup"><span data-stu-id="0fa89-130">Schedule production jobs</span></span>
1. <span data-ttu-id="0fa89-131">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="0fa89-132">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="0fa89-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="0fa89-133">Valitse Rajallinen kapasiteetti -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="0fa89-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="0fa89-134">Valitse Rajallinen materiaali -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="0fa89-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="0fa89-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0fa89-135">Click OK.</span></span>
6. <span data-ttu-id="0fa89-136">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="0fa89-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="0fa89-137">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="0fa89-137">Click All jobs.</span></span>
8. <span data-ttu-id="0fa89-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="0fa89-139">Aloita erätilaus</span><span class="sxs-lookup"><span data-stu-id="0fa89-139">Start the batch order</span></span>
1. <span data-ttu-id="0fa89-140">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="0fa89-140">Click Start.</span></span>
2. <span data-ttu-id="0fa89-141">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0fa89-141">Click the General tab.</span></span>
3. <span data-ttu-id="0fa89-142">Valitse Kirjaa keräysluettelo nyt -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="0fa89-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="0fa89-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0fa89-143">Click OK.</span></span>
5. <span data-ttu-id="0fa89-144">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="0fa89-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="0fa89-145">Valitse Keräysluettelo.</span><span class="sxs-lookup"><span data-stu-id="0fa89-145">Click Picking list.</span></span>
7. <span data-ttu-id="0fa89-146">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0fa89-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0fa89-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-147">Close the page.</span></span>
9. <span data-ttu-id="0fa89-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-148">Close the page.</span></span>
10. <span data-ttu-id="0fa89-149">Valitse Reitityskortti.</span><span class="sxs-lookup"><span data-stu-id="0fa89-149">Click Route card.</span></span>
11. <span data-ttu-id="0fa89-150">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0fa89-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="0fa89-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-151">Close the page.</span></span>
13. <span data-ttu-id="0fa89-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0fa89-152">Close the page.</span></span>

