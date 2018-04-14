--- 
title: "Konsernin sisäisen suunnitelman luominen"
description: "Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b5ed1b47e3e0142a18761f5a47ca12a388305308
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="47bad-103">Konsernin sisäisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="47bad-103">Create an intercompany plan</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47bad-104">Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.</span><span class="sxs-lookup"><span data-stu-id="47bad-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="47bad-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="47bad-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="47bad-106">Määritä konsernin sisäinen suunnitteluryhmä</span><span class="sxs-lookup"><span data-stu-id="47bad-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="47bad-107">Siirry kohtaan Konsernin sisäiset suunnitteluryhmät.</span><span class="sxs-lookup"><span data-stu-id="47bad-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="47bad-108">Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät</span><span class="sxs-lookup"><span data-stu-id="47bad-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="47bad-109">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="47bad-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="47bad-110">Voit esimerkiksi suodattaa Nimi-kenttää arvolla 10.</span><span class="sxs-lookup"><span data-stu-id="47bad-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="47bad-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="47bad-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="47bad-112">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="47bad-112">Click Delete.</span></span>
    * <span data-ttu-id="47bad-113">Tämä vaihe on tarpeen konsernin sisäisen suunnitelma-ajon lyhentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="47bad-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="47bad-114">Konsernin sisäisessä suunnittelussa ajetaan kaikkien suunnitteluryhmän yritysten pääsuunnittelu, ajoitusjärjestyksessä pienimmästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="47bad-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="47bad-115">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="47bad-115">Click Yes.</span></span>
6. <span data-ttu-id="47bad-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="47bad-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="47bad-117">Konsernin sisäisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="47bad-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="47bad-118">Valitse Konsernin sisäinen pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="47bad-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="47bad-119">Toiminto sijaitsee pääsuunnittelun työtilassa.</span><span class="sxs-lookup"><span data-stu-id="47bad-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="47bad-120">Avaa haku napsauttamalla Konsernin sisäinen suunnitteluryhmä -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="47bad-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="47bad-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47bad-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47bad-122">Valitse konsernin sisäinen suunnitteluryhmä 10.</span><span class="sxs-lookup"><span data-stu-id="47bad-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="47bad-123">Kirjoita Konsernin sisäisten suunnitteluiteraatioiden määrä -kenttään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="47bad-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="47bad-124">Konsernin sisäisellä suunnitteluryhmällä 10 on kaksi jäsentä.</span><span class="sxs-lookup"><span data-stu-id="47bad-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="47bad-125">Jotta viiveet voisi täyttää lähdeyrityksestä (USMF) asiakasyritykseen (DEMF), konsernin sisäinen suunnittelu on ajettava molemmissa yrityksissä kahdesti.</span><span class="sxs-lookup"><span data-stu-id="47bad-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="47bad-126">Ensimmäinen iteraatio täyttää kysynnän ja tunnistaa lähdeyrityksen (USMF) viiveet.</span><span class="sxs-lookup"><span data-stu-id="47bad-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="47bad-127">Toisen iteraatio täyttää viiveet yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="47bad-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="47bad-128">Valitse vaihtoehto Ensimmäinen iteraatio -kentässä.</span><span class="sxs-lookup"><span data-stu-id="47bad-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="47bad-129">Valitse Täydellinen laskenta -vaihtoehto Ensimmäinen iteraatio -kentässä.</span><span class="sxs-lookup"><span data-stu-id="47bad-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="47bad-130">Valitse Täydellinen laskenta -vaihtoehto Seuraavat iteraatiot -kentässä.</span><span class="sxs-lookup"><span data-stu-id="47bad-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="47bad-131">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="47bad-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="47bad-132">Tämä vastaa suunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="47bad-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="47bad-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="47bad-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="47bad-134">Näytä suunnitelman tulos</span><span class="sxs-lookup"><span data-stu-id="47bad-134">View the result of the plan</span></span>
1. <span data-ttu-id="47bad-135">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="47bad-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="47bad-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47bad-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47bad-137">Napsauta StaticPlan-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47bad-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="47bad-138">Sinun on oltava USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="47bad-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="47bad-139">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="47bad-139">Click Planned orders.</span></span>


