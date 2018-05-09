---
title: "Varaston kokonaismäärän laskeminen"
description: "Tässä menettelyssä käsitellään varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e7813f9add1c8cf3c2f22aff826daf22f54f348e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="d101e-103">Varaston kokonaismäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="d101e-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d101e-104">Tässä menettelyssä käsitellään varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa.</span><span class="sxs-lookup"><span data-stu-id="d101e-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="d101e-105">Menettely koskee Inventoinnin- ja varastonhallinta -moduulin varastoinnin perustoimintoja. Se ei koske Varastonhallinta-moduulin varastointitoimintoja.</span><span class="sxs-lookup"><span data-stu-id="d101e-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="d101e-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="d101e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="d101e-107">Jos käytät omia tietoja, varmista, että olet määrittänyt tuotteita ja sijainteja ja että olet luonut inventointikirjauskansioille varastokirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="d101e-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="d101e-108">Varastoinventoinnin suorittaa tavallisesti varastotyöntekijä.</span><span class="sxs-lookup"><span data-stu-id="d101e-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="d101e-109">Luo varaston inventointikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="d101e-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="d101e-110">Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Inventointi > Inventointi.</span><span class="sxs-lookup"><span data-stu-id="d101e-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="d101e-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d101e-111">Click New.</span></span>
3. <span data-ttu-id="d101e-112">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d101e-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d101e-113">Valitse luettelosta käytettävä varaston inventointikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="d101e-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="d101e-114">Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston inventointikirjauskansion asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="d101e-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="d101e-115">Avaa haku napsauttamalla Työntekijä-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d101e-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d101e-116">Valitse luettelosta työntekijä, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="d101e-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="d101e-117">Klikkaa Valitse.</span><span class="sxs-lookup"><span data-stu-id="d101e-117">Click Select.</span></span>
8. <span data-ttu-id="d101e-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d101e-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="d101e-119">Tämän kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="d101e-119">Create journal lines</span></span>
1. <span data-ttu-id="d101e-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="d101e-120">Click New.</span></span>
2. <span data-ttu-id="d101e-121">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d101e-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d101e-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d101e-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d101e-123">Jos käytät USMF-yrityksen demotietoja, valitse A0001.</span><span class="sxs-lookup"><span data-stu-id="d101e-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="d101e-124">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d101e-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d101e-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d101e-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d101e-126">Jos käytät USMF-yrityksen demotietoja, valitse toimipaikka 2.</span><span class="sxs-lookup"><span data-stu-id="d101e-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="d101e-127">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d101e-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d101e-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d101e-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d101e-129">Jos käytät USMF-yrityksen demotietoja, valitse varasto 24.</span><span class="sxs-lookup"><span data-stu-id="d101e-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="d101e-130">Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="d101e-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d101e-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="d101e-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d101e-132">Jos käytät USMF-yrityksen demotietoja, valitse sijainti BULK-001.</span><span class="sxs-lookup"><span data-stu-id="d101e-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="d101e-133">Lisää Inventoitu-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="d101e-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="d101e-134">Jos annat inventoitu määrä, joka poikkeaa Varastosaldo-kentässä olevasta numerosta, Määrä-kenttä päivitetään näyttämään ristiriita.</span><span class="sxs-lookup"><span data-stu-id="d101e-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="d101e-135">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d101e-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="d101e-136">Kirjaa varaston inventointikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="d101e-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="d101e-137">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="d101e-137">Click Post.</span></span>
    * <span data-ttu-id="d101e-138">Jos varaston inventointikirjauskansiota kirjatessa kirjataan varastovastaanoton Varastosaldo-kentässä tai varasto-otossa olevasta määrästä eroava inventoitu määrä, varastotaso ja arvo muuttuvat ja kirjanpitotapahtumat muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="d101e-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="d101e-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="d101e-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="d101e-140">Näytä varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="d101e-140">View inventory transactions</span></span>
1. <span data-ttu-id="d101e-141">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="d101e-141">Click Inventory.</span></span>
2. <span data-ttu-id="d101e-142">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="d101e-142">Click Transactions.</span></span>
    * <span data-ttu-id="d101e-143">Tässä näkyvät kaikki liittyvät tapahtumat, jotka luodaan, kun varaston inventointikirjauskansioon kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d101e-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

