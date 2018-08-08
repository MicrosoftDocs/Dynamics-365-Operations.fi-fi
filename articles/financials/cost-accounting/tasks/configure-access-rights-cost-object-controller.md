--- 
title: "Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen"
description: "Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="475e3-103">Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="475e3-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="475e3-104">Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="475e3-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="475e3-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="475e3-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="475e3-106">Kustannusobjektin vastuuhenkilön roolin delegoiminen</span><span class="sxs-lookup"><span data-stu-id="475e3-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="475e3-107">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="475e3-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="475e3-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="475e3-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="475e3-109">Voit esimerkiksi suodattaa Käyttäjän nimi -kenttää arvolla "alicia".</span><span class="sxs-lookup"><span data-stu-id="475e3-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="475e3-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="475e3-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="475e3-111">Valitse Määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="475e3-111">Click Assign roles.</span></span>
5. <span data-ttu-id="475e3-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="475e3-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="475e3-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="475e3-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="475e3-114">Käyttöoikeusluettelon suojauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="475e3-114">Enable access list security</span></span>
1. <span data-ttu-id="475e3-115">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="475e3-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="475e3-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="475e3-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="475e3-117">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="475e3-117">Select Organization.</span></span>  
3. <span data-ttu-id="475e3-118">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="475e3-118">Click Edit.</span></span>
4. <span data-ttu-id="475e3-119">Valitse Käyttöoikeusluettelohierarkia-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="475e3-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="475e3-120">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="475e3-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="475e3-121">Käyttöoikeuksien delegoiminen käyttäjälle</span><span class="sxs-lookup"><span data-stu-id="475e3-121">Assign access rights to user</span></span>
1. <span data-ttu-id="475e3-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="475e3-122">Click New.</span></span>
2. <span data-ttu-id="475e3-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="475e3-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="475e3-124">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="475e3-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="475e3-125">Valitse Järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="475e3-125">Select Admin.</span></span>  
4. <span data-ttu-id="475e3-126">Valitse puussa Organization\CEO\CFO\FIM.</span><span class="sxs-lookup"><span data-stu-id="475e3-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="475e3-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="475e3-127">Click New.</span></span>
6. <span data-ttu-id="475e3-128">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="475e3-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="475e3-129">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="475e3-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="475e3-130">Valitse Alicia.</span><span class="sxs-lookup"><span data-stu-id="475e3-130">Select Alicia.</span></span>  
8. <span data-ttu-id="475e3-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="475e3-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="475e3-132">Käyttöoikeuksien ottaminen käyttöön kustannuslaskennassa</span><span class="sxs-lookup"><span data-stu-id="475e3-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="475e3-133">Valitse Kustannuslaskenta > Asetukset > Parametrit.</span><span class="sxs-lookup"><span data-stu-id="475e3-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="475e3-134">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="475e3-134">Click the General tab.</span></span>
3. <span data-ttu-id="475e3-135">Valitse Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="475e3-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="475e3-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="475e3-136">Click Save.</span></span>
5. <span data-ttu-id="475e3-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="475e3-137">Close the page.</span></span>
6. <span data-ttu-id="475e3-138">Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="475e3-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="475e3-139">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="475e3-139">Click Edit.</span></span>
8. <span data-ttu-id="475e3-140">Valitse Julkaistu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="475e3-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="475e3-141">Jos valitset Kyllä, käyttäjä, jolle on delegoitu jokin seuraavista neljästä roolista, näkee raportit kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö.</span><span class="sxs-lookup"><span data-stu-id="475e3-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="475e3-142">Jos valitset Ei, vain käyttäjä, jolle on delegoitu jokin seuraavista rooleista, näkee raportit: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.</span><span class="sxs-lookup"><span data-stu-id="475e3-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="475e3-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="475e3-143">Click Save.</span></span>


