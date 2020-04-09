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
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a931980add70ddc003d8a7c1a78f451bacbf57d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144493"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="016a0-103">Kustannusobjektin vastuuhenkilön käyttöoikeuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="016a0-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="016a0-104">Tämän menettelyn avulla määritetään kustannusobjektin vastuuhenkilön käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="016a0-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="016a0-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="016a0-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="016a0-106">Kustannusobjektin vastuuhenkilön roolin delegoiminen</span><span class="sxs-lookup"><span data-stu-id="016a0-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="016a0-107">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="016a0-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="016a0-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="016a0-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="016a0-109">Voit esimerkiksi suodattaa Käyttäjän nimi -kenttää arvolla "alicia".</span><span class="sxs-lookup"><span data-stu-id="016a0-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="016a0-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="016a0-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="016a0-111">Valitse Määritä rooleja.</span><span class="sxs-lookup"><span data-stu-id="016a0-111">Click Assign roles.</span></span>
5. <span data-ttu-id="016a0-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="016a0-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="016a0-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="016a0-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="016a0-114">Käyttöoikeusluettelon suojauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="016a0-114">Enable access list security</span></span>
1. <span data-ttu-id="016a0-115">Valitse Kustannuslaskenta > Dimensiot > Dimensiohierarkiat.</span><span class="sxs-lookup"><span data-stu-id="016a0-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="016a0-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="016a0-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="016a0-117">Valitse Organisaatio.</span><span class="sxs-lookup"><span data-stu-id="016a0-117">Select Organization.</span></span>  
3. <span data-ttu-id="016a0-118">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="016a0-118">Click Edit.</span></span>
4. <span data-ttu-id="016a0-119">Valitse Käyttöoikeusluettelohierarkia-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="016a0-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="016a0-120">Valitse Näytä hierarkia.</span><span class="sxs-lookup"><span data-stu-id="016a0-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="016a0-121">Käyttöoikeuksien delegoiminen käyttäjälle</span><span class="sxs-lookup"><span data-stu-id="016a0-121">Assign access rights to user</span></span>
1. <span data-ttu-id="016a0-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="016a0-122">Click New.</span></span>
2. <span data-ttu-id="016a0-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="016a0-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="016a0-124">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="016a0-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="016a0-125">Valitse Järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="016a0-125">Select Admin.</span></span>  
4. <span data-ttu-id="016a0-126">Valitse puussa Organization\CEO\CFO\FIM.</span><span class="sxs-lookup"><span data-stu-id="016a0-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="016a0-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="016a0-127">Click New.</span></span>
6. <span data-ttu-id="016a0-128">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="016a0-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="016a0-129">Syötä tai valitse arvo Käyttäjätunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="016a0-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="016a0-130">Valitse Alicia.</span><span class="sxs-lookup"><span data-stu-id="016a0-130">Select Alicia.</span></span>  
8. <span data-ttu-id="016a0-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="016a0-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="016a0-132">Käyttöoikeuksien ottaminen käyttöön kustannuslaskennassa</span><span class="sxs-lookup"><span data-stu-id="016a0-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="016a0-133">Valitse Kustannuslaskenta > Asetukset > Parametrit.</span><span class="sxs-lookup"><span data-stu-id="016a0-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="016a0-134">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="016a0-134">Click the General tab.</span></span>
3. <span data-ttu-id="016a0-135">Valitse Ota käyttöön katseluoikeus kustannusobjektin dimension jäsenille -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="016a0-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="016a0-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="016a0-136">Click Save.</span></span>
5. <span data-ttu-id="016a0-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="016a0-137">Close the page.</span></span>
6. <span data-ttu-id="016a0-138">Valitse Kustannuslaskenta > Asetukset > Kustannusseurannan työtilan konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="016a0-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="016a0-139">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="016a0-139">Click Edit.</span></span>
8. <span data-ttu-id="016a0-140">Valitse Julkaistu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="016a0-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="016a0-141">Jos valitset Kyllä, käyttäjä, jolle on delegoitu jokin seuraavista neljästä roolista, näkee raportit kustannusseurannan työtilassa: kustannuslaskennan hallinta, kustannuslaskija, kustannuslaskijan apulainen tai kustannusobjektin vastuuhenkilö.</span><span class="sxs-lookup"><span data-stu-id="016a0-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="016a0-142">Jos valitset Ei, vain käyttäjä, jolle on delegoitu jokin seuraavista rooleista, näkee raportit: kustannuslaskennan hallinta, kustannuslaskija tai kustannuslaskijan apulainen.</span><span class="sxs-lookup"><span data-stu-id="016a0-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="016a0-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="016a0-143">Click Save.</span></span>

