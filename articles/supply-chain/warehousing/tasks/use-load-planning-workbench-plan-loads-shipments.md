---
title: Suunnittele kuormat ja lähetykset kuormasuunnittelun työtilassa
description: Tässä menettelyssä kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564790"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="6d782-103">Suunnittele kuormat ja lähetykset kuormasuunnittelun työtilassa</span><span class="sxs-lookup"><span data-stu-id="6d782-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d782-104">Tässä menettelyssä kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.</span><span class="sxs-lookup"><span data-stu-id="6d782-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="6d782-105">Ensimmäiseksi luodaan edellytyksenä oleva myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="6d782-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="6d782-106">Tämä menettely on osa kuljetuskoordinaattorin päivittäistä työtä.</span><span class="sxs-lookup"><span data-stu-id="6d782-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="6d782-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="6d782-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="6d782-108">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="6d782-108">Create a sales order</span></span>
1. <span data-ttu-id="6d782-109">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="6d782-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="6d782-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6d782-110">Click New.</span></span>
3. <span data-ttu-id="6d782-111">Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6d782-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6d782-112">Valitse tili US-004.</span><span class="sxs-lookup"><span data-stu-id="6d782-112">Select account US-004.</span></span>
5. <span data-ttu-id="6d782-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6d782-113">Click OK.</span></span>
6. <span data-ttu-id="6d782-114">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6d782-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6d782-115">Valitse nimike A0001.</span><span class="sxs-lookup"><span data-stu-id="6d782-115">Select item A0001.</span></span>
    * <span data-ttu-id="6d782-116">A0001 on kuljetustenhallinnan käytössä.</span><span class="sxs-lookup"><span data-stu-id="6d782-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="6d782-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6d782-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6d782-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6d782-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="6d782-119">Syötä Varasto-kenttään 24.</span><span class="sxs-lookup"><span data-stu-id="6d782-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="6d782-120">Valitse tässä esimerkissä varasto 24.</span><span class="sxs-lookup"><span data-stu-id="6d782-120">In this example select warehouse 24.</span></span> <span data-ttu-id="6d782-121">Kuljetuksenhallinta ja varastonhallinnan lisätoiminnot ovat tässä varastossa käytössä.</span><span class="sxs-lookup"><span data-stu-id="6d782-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="6d782-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6d782-122">Click Save.</span></span>
12. <span data-ttu-id="6d782-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d782-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="6d782-124">Uuden kuorman luominen</span><span class="sxs-lookup"><span data-stu-id="6d782-124">Create a new load</span></span>
1. <span data-ttu-id="6d782-125">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="6d782-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="6d782-126">Valitse Myyntirivit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6d782-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="6d782-127">Muodostetaan nyt juuri luodulle myyntitilaukselle kuorma.</span><span class="sxs-lookup"><span data-stu-id="6d782-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="6d782-128">Kuormat voidaan muodostaa tarjonnan ja kysynnän perusteella ostotilauksista, siirtotilauksista ja myyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="6d782-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="6d782-129">Valitse toimintoruudussa Tarjonta ja kysyntä.</span><span class="sxs-lookup"><span data-stu-id="6d782-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="6d782-130">Valitse Uuteen kuormaan.</span><span class="sxs-lookup"><span data-stu-id="6d782-130">Click To new load.</span></span>
5. <span data-ttu-id="6d782-131">Avaa haku valitsemalla Kuorman mallitunnus -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6d782-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6d782-132">Kuormamalli määrittää koko kuorman painon ja tilavuuden enimmäismitat.</span><span class="sxs-lookup"><span data-stu-id="6d782-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="6d782-133">Kuormamalli voi esittää esimerkiksi kontin tai kuorma-auton koon.</span><span class="sxs-lookup"><span data-stu-id="6d782-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="6d782-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6d782-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6d782-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6d782-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="6d782-136">Kuorman hinnan ja reitityksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6d782-136">Rate and route the load</span></span>
1. <span data-ttu-id="6d782-137">Valitse Hinnoittelu ja reititys.</span><span class="sxs-lookup"><span data-stu-id="6d782-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="6d782-138">Valitse Hinnan ja reitin työtila.</span><span class="sxs-lookup"><span data-stu-id="6d782-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="6d782-139">Valitse Hintavertailu.</span><span class="sxs-lookup"><span data-stu-id="6d782-139">Click Rate shop.</span></span>
4. <span data-ttu-id="6d782-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6d782-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6d782-141">Valitse Liitä.</span><span class="sxs-lookup"><span data-stu-id="6d782-141">Click Assign.</span></span>
6. <span data-ttu-id="6d782-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d782-142">Close the page.</span></span>
7. <span data-ttu-id="6d782-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d782-143">Close the page.</span></span>

