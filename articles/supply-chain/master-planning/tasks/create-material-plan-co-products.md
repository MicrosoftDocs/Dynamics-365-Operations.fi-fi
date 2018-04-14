--- 
title: Oheistuotteiden materiaalisuunnitelman luominen
description: Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 77fa282401a7c2b0115235f1bd902998e9eed7c1
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="2a09e-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="2a09e-103">Create a material plan for co-products</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a09e-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="2a09e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="2a09e-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="2a09e-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="2a09e-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="2a09e-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="2a09e-107">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="2a09e-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="2a09e-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="2a09e-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="2a09e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2a09e-109">Click New.</span></span>
4. <span data-ttu-id="2a09e-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="2a09e-110">Click Sales order.</span></span>
5. <span data-ttu-id="2a09e-111">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a09e-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="2a09e-112">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="2a09e-112">Example: US-001</span></span>  
6. <span data-ttu-id="2a09e-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2a09e-113">Click OK.</span></span>
7. <span data-ttu-id="2a09e-114">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a09e-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2a09e-115">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="2a09e-115">Example: P6003</span></span>  
8. <span data-ttu-id="2a09e-116">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a09e-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2a09e-117">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="2a09e-117">Example: 50000</span></span>  
9. <span data-ttu-id="2a09e-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2a09e-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="2a09e-119">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="2a09e-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="2a09e-120">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="2a09e-120">Click Master planning.</span></span>
2. <span data-ttu-id="2a09e-121">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2a09e-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2a09e-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a09e-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2a09e-123">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="2a09e-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="2a09e-124">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="2a09e-124">Click Run.</span></span>
5. <span data-ttu-id="2a09e-125">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="2a09e-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="2a09e-126">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="2a09e-126">Click Filter.</span></span>
7. <span data-ttu-id="2a09e-127">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="2a09e-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="2a09e-128">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2a09e-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="2a09e-129">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="2a09e-129">Example: P6003</span></span>  
9. <span data-ttu-id="2a09e-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2a09e-130">Click OK.</span></span>
10. <span data-ttu-id="2a09e-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2a09e-131">Click OK.</span></span>
11. <span data-ttu-id="2a09e-132">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="2a09e-132">Click Planned orders.</span></span>
12. <span data-ttu-id="2a09e-133">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="2a09e-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2a09e-134">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="2a09e-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="2a09e-135">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="2a09e-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="2a09e-136">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2a09e-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2a09e-137">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="2a09e-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="2a09e-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a09e-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="2a09e-139">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="2a09e-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="2a09e-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2a09e-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2a09e-141">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="2a09e-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="2a09e-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09e-142">Close the page.</span></span>


