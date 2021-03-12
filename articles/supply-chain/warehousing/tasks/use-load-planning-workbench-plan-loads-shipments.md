---
title: Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa
description: Tässä aiheessa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976810"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="9b5bb-103">Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="9b5bb-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b5bb-104">Tässä aiheessa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="9b5bb-105">Ensimmäiseksi luodaan edellytyksenä oleva myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="9b5bb-106">Tämä menettely on osa kuljetuskoordinaattorin päivittäistä työtä.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="9b5bb-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="9b5bb-108">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="9b5bb-108">Create a sales order</span></span>
1. <span data-ttu-id="9b5bb-109">Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="9b5bb-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-110">Select **New**.</span></span>
3. <span data-ttu-id="9b5bb-111">Avaa haku valitsemalla **Asiakastili**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9b5bb-112">Valitse tili **US-004**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="9b5bb-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-113">Select **OK**.</span></span>
6. <span data-ttu-id="9b5bb-114">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9b5bb-115">Valitse nimike **A0001**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-115">Select item **A0001**.</span></span> <span data-ttu-id="9b5bb-116">**A0001** on kuljetustenhallinnan käytössä.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="9b5bb-117">Avaa haku valitsemalla **Toimipaikka**-kentässä avattavan valikon painike ja valitse nimike.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="9b5bb-118">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="9b5bb-119">Kirjoita tässä esimerkissä **Varasto**-kenttään 24.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="9b5bb-120">Kuljetuksenhallinta ja varastonhallinnan lisätoiminnot ovat tässä varastossa käytössä.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="9b5bb-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-121">Select **Save**.</span></span>
12. <span data-ttu-id="9b5bb-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="9b5bb-123">Uuden kuorman luominen</span><span class="sxs-lookup"><span data-stu-id="9b5bb-123">Create a new load</span></span>
1. <span data-ttu-id="9b5bb-124">Siirry kohtaan **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="9b5bb-125">Valitse **Myyntirivit**-välilehti. Muodostetaan nyt juuri luodulle myyntitilaukselle kuorma.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="9b5bb-126">Kuormat voidaan muodostaa tarjonnan ja kysynnän perusteella ostotilauksista, siirtotilauksista ja myyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="9b5bb-127">Valitse toimintoruudussa **Tarjonta ja kysyntä**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="9b5bb-128">Valitse **Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-128">Select **To new load**.</span></span>
5. <span data-ttu-id="9b5bb-129">Avaa haku valitsemalla **Kuorman mallitunnus** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="9b5bb-130">Kuormamalli määrittää koko kuorman painon ja tilavuuden enimmäismitat.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="9b5bb-131">Kuormamalli voi esittää esimerkiksi kontin tai kuorma-auton koon.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="9b5bb-132">Valitse nimike.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-132">Select an item.</span></span>
6. <span data-ttu-id="9b5bb-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="9b5bb-134">Kuorman hinnan ja reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9b5bb-134">Rate and route the load</span></span>
1. <span data-ttu-id="9b5bb-135">Valitse **Hinnoittelu ja reititys**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="9b5bb-136">Valitse **Hinnan ja reitin työtila**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="9b5bb-137">Valitse **Hintavertailu**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="9b5bb-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9b5bb-139">Valitse **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-139">Select **Assign**.</span></span>
6. <span data-ttu-id="9b5bb-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9b5bb-140">Close the page.</span></span>

