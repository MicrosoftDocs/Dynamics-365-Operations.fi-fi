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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b64ababa618d58feb6095704e5978295060c96f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261113"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="648a6-103">Konsernin sisäisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="648a6-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="648a6-104">Tässä menettelyssä kuvataan, miten luot konsernin sisäisen suunnitelman.</span><span class="sxs-lookup"><span data-stu-id="648a6-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="648a6-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="648a6-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="648a6-106">Määritä konsernin sisäinen suunnitteluryhmä</span><span class="sxs-lookup"><span data-stu-id="648a6-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="648a6-107">Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Asetukset > Konsernin sisäiset suunnitteluryhmät.**</span><span class="sxs-lookup"><span data-stu-id="648a6-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="648a6-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="648a6-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="648a6-109">Voit esimerkiksi suodattaa Nimi-kenttää arvolla 10.</span><span class="sxs-lookup"><span data-stu-id="648a6-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="648a6-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="648a6-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="648a6-111">Valitse **Poista**.</span><span class="sxs-lookup"><span data-stu-id="648a6-111">Click **Delete**.</span></span> <span data-ttu-id="648a6-112">Tämä vaihe on tarpeen konsernin sisäisen suunnitelma-ajon lyhentämiseksi.</span><span class="sxs-lookup"><span data-stu-id="648a6-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="648a6-113">Konsernin sisäisessä suunnittelussa ajetaan kaikkien suunnitteluryhmän yritysten pääsuunnittelu, ajoitusjärjestyksessä pienimmästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="648a6-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="648a6-114">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="648a6-114">Click **Yes**.</span></span>
6. <span data-ttu-id="648a6-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="648a6-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="648a6-116">Konserniyritysten välisen suunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="648a6-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="648a6-117">Siirry **siirtymisruudussa** **Moduulit > Pääsuunnittelu > Työtilat > Pääsunnittelu.**</span><span class="sxs-lookup"><span data-stu-id="648a6-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="648a6-118">Valitse **Konsernin sisäinen pääsuunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="648a6-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="648a6-119">Avaa haku napsauttamalla **Konsernin sisäinen suunnitteluryhmä** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="648a6-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="648a6-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="648a6-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="648a6-121">Valitse konsernin sisäinen suunnitteluryhmä 10.</span><span class="sxs-lookup"><span data-stu-id="648a6-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="648a6-122">Kirjoita **Konsernin sisäisten suunnitteluiteraatioiden määrä** -kenttään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="648a6-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="648a6-123">Konsernin sisäisellä suunnitteluryhmällä 10 on kaksi jäsentä.</span><span class="sxs-lookup"><span data-stu-id="648a6-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="648a6-124">Jotta viiveet voisi täyttää lähdeyrityksestä (USMF) asiakasyritykseen (DEMF), konsernin sisäinen suunnittelu on ajettava molemmissa yrityksissä kahdesti.</span><span class="sxs-lookup"><span data-stu-id="648a6-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="648a6-125">Ensimmäinen iteraatio täyttää kysynnän ja tunnistaa lähdeyrityksen (USMF) viiveet.</span><span class="sxs-lookup"><span data-stu-id="648a6-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="648a6-126">Toisen iteraatio täyttää viiveet yritysten välillä.</span><span class="sxs-lookup"><span data-stu-id="648a6-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="648a6-127">Valitse Täydellinen laskenta -vaihtoehto **Ensimmäinen iteraatio** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="648a6-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="648a6-128">Valitse Täydellinen laskenta -vaihtoehto **Seuraavat iteraatiot** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="648a6-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="648a6-129">Syötä **Säikeiden määrä** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="648a6-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="648a6-130">Tämä vastaa suunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="648a6-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="648a6-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="648a6-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="648a6-132">Näytä suunnitelman tulos</span><span class="sxs-lookup"><span data-stu-id="648a6-132">View the result of the plan</span></span>
1. <span data-ttu-id="648a6-133">Avaa haku valitsemalla **Suunnitelma**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="648a6-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="648a6-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="648a6-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="648a6-135">Napsauta StaticPlan-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="648a6-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="648a6-136">Sinun on oltava USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="648a6-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="648a6-137">Valitse **Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="648a6-137">Click **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]