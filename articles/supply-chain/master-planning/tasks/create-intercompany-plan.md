---
title: Konsernin sisäisen suunnitelman luominen
description: Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426933"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="75b0e-103">Konsernin sisäisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="75b0e-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75b0e-104">Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.</span><span class="sxs-lookup"><span data-stu-id="75b0e-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="75b0e-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="75b0e-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="75b0e-106">Määritä konsernin sisäinen suunnitteluryhmä</span><span class="sxs-lookup"><span data-stu-id="75b0e-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="75b0e-107">Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät.**</span><span class="sxs-lookup"><span data-stu-id="75b0e-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="75b0e-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="75b0e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="75b0e-109">Voit esimerkiksi suodattaa Nimi-kenttää arvolla 10.</span><span class="sxs-lookup"><span data-stu-id="75b0e-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="75b0e-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="75b0e-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="75b0e-111">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="75b0e-111">Click **Delete**.</span></span> <span data-ttu-id="75b0e-112">Tämä vaihe on tarpeen konsernin sisäisen suunnitelma-ajon lyhentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="75b0e-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="75b0e-113">Konsernin sisäisessä suunnittelussa ajetaan kaikkien suunnitteluryhmän yritysten pääsuunnittelu, ajoitusjärjestyksessä pienimmästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="75b0e-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="75b0e-114">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="75b0e-114">Click **Yes**.</span></span>
6. <span data-ttu-id="75b0e-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="75b0e-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="75b0e-116">Konserniyritysten välisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="75b0e-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="75b0e-117">Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Työtilat > Pääsunnittelu.**</span><span class="sxs-lookup"><span data-stu-id="75b0e-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="75b0e-118">Valitse **Konsernin sisäinen pääsuunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="75b0e-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="75b0e-119">Avaa haku napsauttamalla **Konsernin sisäinen suunnitteluryhmä** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="75b0e-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="75b0e-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="75b0e-121">Valitse konsernin sisäinen suunnitteluryhmä 10.</span><span class="sxs-lookup"><span data-stu-id="75b0e-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="75b0e-122">Kirjoita **Konsernin sisäisten suunnitteluiteraatioiden määrä** -kenttään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="75b0e-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="75b0e-123">Konsernin sisäisellä suunnitteluryhmällä 10 on kaksi jäsentä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="75b0e-124">Jotta viiveet voisi täyttää lähdeyrityksestä (USMF) asiakasyritykseen (DEMF), konsernin sisäinen suunnittelu on ajettava molemmissa yrityksissä kahdesti.</span><span class="sxs-lookup"><span data-stu-id="75b0e-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="75b0e-125">Ensimmäinen iteraatio täyttää kysynnän ja tunnistaa lähdeyrityksen (USMF) viiveet.</span><span class="sxs-lookup"><span data-stu-id="75b0e-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="75b0e-126">Toisen iteraatio täyttää viiveet yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="75b0e-127">Valitse Täydellinen laskenta -vaihtoehto **Ensimmäinen iteraatio** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="75b0e-128">Valitse Täydellinen laskenta -vaihtoehto **Seuraavat iteraatiot** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="75b0e-129">Syötä **Säikeiden määrä** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="75b0e-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="75b0e-130">Tämä vastaa suunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="75b0e-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="75b0e-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75b0e-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="75b0e-132">Näytä suunnitelman tulos</span><span class="sxs-lookup"><span data-stu-id="75b0e-132">View the result of the plan</span></span>
1. <span data-ttu-id="75b0e-133">Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="75b0e-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="75b0e-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="75b0e-135">Napsauta StaticPlan-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="75b0e-136">Sinun on oltava USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="75b0e-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="75b0e-137">Valitse **Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="75b0e-137">Click **Planned orders**.</span></span>

