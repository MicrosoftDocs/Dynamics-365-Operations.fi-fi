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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0b687-103">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="0b687-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b687-104">Tuotannon suunnittelija suunnittelee materiaalitarpeet nimikkeille, jotka ovat reseptin oheistuotteita.</span><span class="sxs-lookup"><span data-stu-id="0b687-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="0b687-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="0b687-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="0b687-106">Oheistuotteen tarpeen luominen</span><span class="sxs-lookup"><span data-stu-id="0b687-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="0b687-107">Siirry oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="0b687-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="0b687-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="0b687-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="0b687-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0b687-109">Click New.</span></span>
4. <span data-ttu-id="0b687-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="0b687-110">Click Sales order.</span></span>
5. <span data-ttu-id="0b687-111">Kirjoita arvo Asiakastili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b687-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="0b687-112">Esimerkki: US-001</span><span class="sxs-lookup"><span data-stu-id="0b687-112">Example: US-001</span></span>  
6. <span data-ttu-id="0b687-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b687-113">Click OK.</span></span>
7. <span data-ttu-id="0b687-114">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b687-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0b687-115">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="0b687-115">Example: P6003</span></span>  
8. <span data-ttu-id="0b687-116">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b687-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0b687-117">Esimerkki: 50 000</span><span class="sxs-lookup"><span data-stu-id="0b687-117">Example: 50000</span></span>  
9. <span data-ttu-id="0b687-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0b687-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0b687-119">Oheistuotteiden materiaalisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="0b687-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="0b687-120">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="0b687-120">Click Master planning.</span></span>
2. <span data-ttu-id="0b687-121">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="0b687-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0b687-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0b687-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b687-123">Esimerkki: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0b687-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="0b687-124">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="0b687-124">Click Run.</span></span>
5. <span data-ttu-id="0b687-125">Laajenna tai tiivistä Sisällytettävät tietueet -osa.</span><span class="sxs-lookup"><span data-stu-id="0b687-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="0b687-126">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="0b687-126">Click Filter.</span></span>
7. <span data-ttu-id="0b687-127">Valitse luettelosta rivi Nimiketunnus-kentälle.</span><span class="sxs-lookup"><span data-stu-id="0b687-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="0b687-128">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b687-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0b687-129">Esimerkki: P6003</span><span class="sxs-lookup"><span data-stu-id="0b687-129">Example: P6003</span></span>  
9. <span data-ttu-id="0b687-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b687-130">Click OK.</span></span>
10. <span data-ttu-id="0b687-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b687-131">Click OK.</span></span>
11. <span data-ttu-id="0b687-132">Valitse Suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="0b687-132">Click Planned orders.</span></span>
12. <span data-ttu-id="0b687-133">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="0b687-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0b687-134">Voit esimerkiksi suodattaa Nimiketunnus-kenttää arvolla P6000.</span><span class="sxs-lookup"><span data-stu-id="0b687-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0b687-135">Suodata sellaisen reseptinimikkeen perusteella, jolla on sen nimikkeen oheistuote, jolle myyntitilaus luotiin.</span><span class="sxs-lookup"><span data-stu-id="0b687-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="0b687-136">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b687-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0b687-137">Valitse mikä tahansa suodattimen palauttamista riveistä.</span><span class="sxs-lookup"><span data-stu-id="0b687-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="0b687-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0b687-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0b687-139">Laajenna tai tiivistä Tarvekohdistus-osa.</span><span class="sxs-lookup"><span data-stu-id="0b687-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="0b687-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0b687-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b687-141">Suunniteltu tilaus on tarvekohdistettu oheistuotteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="0b687-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="0b687-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b687-142">Close the page.</span></span>


