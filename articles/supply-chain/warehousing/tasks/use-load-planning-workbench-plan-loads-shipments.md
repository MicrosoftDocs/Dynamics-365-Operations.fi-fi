---
title: Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa
description: Tässä aiheessa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145876"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="bd0b8-103">Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="bd0b8-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd0b8-104">Tässä aiheessa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="bd0b8-105">Ensimmäiseksi luodaan edellytyksenä oleva myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="bd0b8-106">Tämä menettely on osa kuljetuskoordinaattorin päivittäistä työtä.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="bd0b8-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="bd0b8-108">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="bd0b8-108">Create a sales order</span></span>
1. <span data-ttu-id="bd0b8-109">Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="bd0b8-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-110">Select **New**.</span></span>
3. <span data-ttu-id="bd0b8-111">Avaa haku valitsemalla **Asiakastili**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bd0b8-112">Valitse tili **US-004**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="bd0b8-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-113">Select **OK**.</span></span>
6. <span data-ttu-id="bd0b8-114">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bd0b8-115">Valitse nimike **A0001**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-115">Select item **A0001**.</span></span> <span data-ttu-id="bd0b8-116">**A0001** on kuljetustenhallinnan käytössä.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="bd0b8-117">Avaa haku valitsemalla **Toimipaikka**-kentässä avattavan valikon painike ja valitse nimike.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="bd0b8-118">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="bd0b8-119">Kirjoita tässä esimerkissä **Varasto**-kenttään 24.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="bd0b8-120">Kuljetuksenhallinta ja varastonhallinnan lisätoiminnot ovat tässä varastossa käytössä.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="bd0b8-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-121">Select **Save**.</span></span>
12. <span data-ttu-id="bd0b8-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="bd0b8-123">Uuden kuorman luominen</span><span class="sxs-lookup"><span data-stu-id="bd0b8-123">Create a new load</span></span>
1. <span data-ttu-id="bd0b8-124">Siirry kohtaan **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="bd0b8-125">Valitse **Myyntirivit**-välilehti. Muodostetaan nyt juuri luodulle myyntitilaukselle kuorma.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="bd0b8-126">Kuormat voidaan muodostaa tarjonnan ja kysynnän perusteella ostotilauksista, siirtotilauksista ja myyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="bd0b8-127">Valitse toimintoruudussa **Tarjonta ja kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="bd0b8-128">Valitse **Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-128">Select **To new load**.</span></span>
5. <span data-ttu-id="bd0b8-129">Avaa haku valitsemalla **Kuorman mallitunnus** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="bd0b8-130">Kuormamalli määrittää koko kuorman painon ja tilavuuden enimmäismitat.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="bd0b8-131">Kuormamalli voi esittää esimerkiksi kontin tai kuorma-auton koon.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="bd0b8-132">Valitse nimike.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-132">Select an item.</span></span>
6. <span data-ttu-id="bd0b8-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="bd0b8-134">Kuorman hinnan ja reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bd0b8-134">Rate and route the load</span></span>
1. <span data-ttu-id="bd0b8-135">Valitse **Hinnoittelu ja reititys**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="bd0b8-136">Valitse **Hinnan ja reitin työtila**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="bd0b8-137">Valitse **Hintavertailu**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="bd0b8-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bd0b8-139">Valitse **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-139">Select **Assign**.</span></span>
6. <span data-ttu-id="bd0b8-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="bd0b8-140">Close the page.</span></span>

