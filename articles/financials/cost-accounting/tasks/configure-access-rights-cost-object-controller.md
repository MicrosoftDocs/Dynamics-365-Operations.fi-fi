---
title: Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen
description: Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "351168"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="c4009-103">Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c4009-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4009-104">Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="c4009-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="c4009-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="c4009-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="c4009-106">Kustannusobjektin vastuuhenkilön roolin delegoiminen</span><span class="sxs-lookup"><span data-stu-id="c4009-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="c4009-107">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="c4009-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c4009-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="c4009-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c4009-109">Voit esimerkiksi suodattaa Käyttäjän nimi -kenttää arvolla "alicia".</span><span class="sxs-lookup"><span data-stu-id="c4009-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="c4009-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c4009-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c4009-111">Valitse Määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="c4009-111">Click Assign roles.</span></span>
5. <span data-ttu-id="c4009-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c4009-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c4009-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4009-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="c4009-114">Käyttöoikeusluettelon suojauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="c4009-114">Enable access list security</span></span>
1. <span data-ttu-id="c4009-115">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="c4009-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="c4009-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c4009-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c4009-117">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="c4009-117">Select Organization.</span></span>  
3. <span data-ttu-id="c4009-118">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c4009-118">Click Edit.</span></span>
4. <span data-ttu-id="c4009-119">Valitse Käyttöoikeusluettelohierarkia-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c4009-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="c4009-120">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="c4009-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="c4009-121">Käyttöoikeuksien delegoiminen käyttäjälle</span><span class="sxs-lookup"><span data-stu-id="c4009-121">Assign access rights to user</span></span>
1. <span data-ttu-id="c4009-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c4009-122">Click New.</span></span>
2. <span data-ttu-id="c4009-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c4009-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c4009-124">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4009-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="c4009-125">Valitse Järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="c4009-125">Select Admin.</span></span>  
4. <span data-ttu-id="c4009-126">Valitse puussa Organization\CEO\CFO\FIM.</span><span class="sxs-lookup"><span data-stu-id="c4009-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="c4009-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c4009-127">Click New.</span></span>
6. <span data-ttu-id="c4009-128">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c4009-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c4009-129">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4009-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="c4009-130">Valitse Alicia.</span><span class="sxs-lookup"><span data-stu-id="c4009-130">Select Alicia.</span></span>  
8. <span data-ttu-id="c4009-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c4009-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="c4009-132">Käyttöoikeuksien ottaminen käyttöön kustannuslaskennassa</span><span class="sxs-lookup"><span data-stu-id="c4009-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="c4009-133">Valitse Kustannuslaskenta > Asetukset > Parametrit.</span><span class="sxs-lookup"><span data-stu-id="c4009-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="c4009-134">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c4009-134">Click the General tab.</span></span>
3. <span data-ttu-id="c4009-135">Valitse Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c4009-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="c4009-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c4009-136">Click Save.</span></span>
5. <span data-ttu-id="c4009-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c4009-137">Close the page.</span></span>
6. <span data-ttu-id="c4009-138">Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="c4009-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="c4009-139">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="c4009-139">Click Edit.</span></span>
8. <span data-ttu-id="c4009-140">Valitse Julkaistu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c4009-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="c4009-141">Jos valitset Kyllä, käyttäjä, jolle on delegoitu jokin seuraavista neljästä roolista, näkee raportit kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö.</span><span class="sxs-lookup"><span data-stu-id="c4009-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="c4009-142">Jos valitset Ei, vain käyttäjä, jolle on delegoitu jokin seuraavista rooleista, näkee raportit: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.</span><span class="sxs-lookup"><span data-stu-id="c4009-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="c4009-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c4009-143">Click Save.</span></span>

