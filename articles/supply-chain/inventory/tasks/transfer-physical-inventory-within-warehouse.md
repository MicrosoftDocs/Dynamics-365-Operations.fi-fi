---
title: "Fyysisen varaston siirtäminen varastossa"
description: "Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/12/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="e1669-103">Fyysisen varaston siirtäminen varastossa</span><span class="sxs-lookup"><span data-stu-id="e1669-103">Transfer physical inventory within the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1669-104">Tässä menettelyssä käsitellään varastosiirtokirjauskansion luominen ja kirjaaminen, jotta nimikkeen siirto varastosijainnista toiseen voidaan rekisteröidä.</span><span class="sxs-lookup"><span data-stu-id="e1669-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="e1669-105">Ennen aloittamista varastosiirroille on oltava määritettynä varastokirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="e1669-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="e1669-106">Voit käyttää menettelyssä USMF-yrityksen demotiedoissa näytettyjä esimerkkiarvoja tai omia tietojasi, jos sinulla on määritettyjä tuotteita ja sijainteja.</span><span class="sxs-lookup"><span data-stu-id="e1669-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="e1669-107">Yleensä varastotyöntekijä tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="e1669-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="e1669-108">Luo varastosiirtokirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e1669-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="e1669-109">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="e1669-109">Go to Transfer.</span></span>
2. <span data-ttu-id="e1669-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1669-110">Click New.</span></span>
3. <span data-ttu-id="e1669-111">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1669-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e1669-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e1669-112">Click OK.</span></span>
    * <span data-ttu-id="e1669-113">Kunkin kirjauskansion rivin määrittämiseen on lähtö- ja kohdedimensioasetus.</span><span class="sxs-lookup"><span data-stu-id="e1669-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="e1669-114">Ne ovat välttämättömiä tässä kirjauskansiotyypissä.</span><span class="sxs-lookup"><span data-stu-id="e1669-114">These are essential for this journal type.</span></span> <span data-ttu-id="e1669-115">Voit siirtää nimikkeitä sijainteihin eri säännöillä.</span><span class="sxs-lookup"><span data-stu-id="e1669-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="e1669-116">Tässä esimerkissä nimike siirretään samassa varastossa rekisterikilvellä ohjatusta sijainnista sijaintiin, jota ei ohjata rekisterikilvellä.</span><span class="sxs-lookup"><span data-stu-id="e1669-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="e1669-117">Tämän kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="e1669-117">Create journal lines</span></span>
1. <span data-ttu-id="e1669-118">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e1669-118">Click New.</span></span>
2. <span data-ttu-id="e1669-119">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e1669-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-120">Jos käytössä on USMF, voit valita A0001.</span><span class="sxs-lookup"><span data-stu-id="e1669-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="e1669-121">Anna tai valitse Toimipaikasta-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-122">Jos käytössä on USMF, voit valita 2.</span><span class="sxs-lookup"><span data-stu-id="e1669-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="e1669-123">Anna tai valitse Toimipaikkaan-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-124">Jos käytössä on USMF, voit valita 2.</span><span class="sxs-lookup"><span data-stu-id="e1669-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="e1669-125">Anna tai valitse Varastosta-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-126">Jos käytössä on USMF, voit valita 24.</span><span class="sxs-lookup"><span data-stu-id="e1669-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="e1669-127">Anna tai valitse Varastoon-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-128">Jos käytössä on USMF, voit valita 24.</span><span class="sxs-lookup"><span data-stu-id="e1669-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="e1669-129">Anna tai valitse Lähtösijainti -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-130">Jos käytössä on USMF, voit valita FL-001.</span><span class="sxs-lookup"><span data-stu-id="e1669-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="e1669-131">Anna tai valitse Kohdesijainti-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-132">Jos käytössä on USMF, voit valita BULK-001.</span><span class="sxs-lookup"><span data-stu-id="e1669-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="e1669-133">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e1669-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="e1669-134">Valitse Varastodimensiot-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e1669-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="e1669-135">Anna tai valitse Rekisterikilpi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e1669-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="e1669-136">Jos käytössä on USMF, voit valita 24.</span><span class="sxs-lookup"><span data-stu-id="e1669-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="e1669-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e1669-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="e1669-138">Kirjaa varastosiirtokirjauskansio</span><span class="sxs-lookup"><span data-stu-id="e1669-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="e1669-139">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="e1669-139">Click Post.</span></span>
2. <span data-ttu-id="e1669-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e1669-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e1669-141">Näytä varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="e1669-141">View inventory transactions</span></span>
1. <span data-ttu-id="e1669-142">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="e1669-142">Click Inventory.</span></span>
2. <span data-ttu-id="e1669-143">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e1669-143">Click Transactions.</span></span>
    * <span data-ttu-id="e1669-144">Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.</span><span class="sxs-lookup"><span data-stu-id="e1669-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

