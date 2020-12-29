---
title: Lisää kanban-määrän laskentakäytäntö kanban-sääntöön
description: Tässä menettelyssä keskitytään kanban-määrän laskentakäytännön luomiseen ja sen lisäämiseen kanban-sääntöön kanbanin koon ja määrien optimoimista varten.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 039c4aaa355cf2b850ded06913e8e39ee8cac543
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426806"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="71266-103">Lisää kanban-määrän laskentakäytäntö kanban-sääntöön</span><span class="sxs-lookup"><span data-stu-id="71266-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71266-104">Tässä menettelyssä keskitytään kanban-määrän laskentakäytännön luomiseen ja sen lisäämiseen kanban-sääntöön kanbanin koon ja määrien optimoimista varten.</span><span class="sxs-lookup"><span data-stu-id="71266-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="71266-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="71266-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71266-106">Tämä menettely on tarkoitettu arvovirtaa hallitsevalle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="71266-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="71266-107">Tämä menettely on Laske kanban-määräehdotukset -menettelyn luomisen edellytys.</span><span class="sxs-lookup"><span data-stu-id="71266-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="71266-108">Uuden kanban-määrän laskentakäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="71266-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="71266-109">Siirry kohtaan Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Kanban-määrän laskentakäytännöt.</span><span class="sxs-lookup"><span data-stu-id="71266-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="71266-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="71266-110">Click New.</span></span>
3. <span data-ttu-id="71266-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="71266-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="71266-112">Syötä esimerkiksi arvo Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="71266-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="71266-113">Avaa haku valitsemalla Pääsuunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="71266-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="71266-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="71266-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71266-115">Valitse StaticPlan, kun haluat laskea kysynnän.</span><span class="sxs-lookup"><span data-stu-id="71266-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="71266-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="71266-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="71266-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="71266-117">Click Save.</span></span>
8. <span data-ttu-id="71266-118">Syötä Kanban-määrä vähintään -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="71266-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="71266-119">Tämä on kanbanien lisänumero, joka sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="71266-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="71266-120">Määritä turvallisuuskertoimeksi 1.</span><span class="sxs-lookup"><span data-stu-id="71266-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="71266-121">Tämä on kerroin, jota käytetään varmuusvaraston lisämäärän laskennassa.</span><span class="sxs-lookup"><span data-stu-id="71266-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="71266-122">Syötä Jäljellä olevat päivät -kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="71266-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="71266-123">Tämä on niiden päivien lukumäärä ennen kanban-määrän laskentapäivämäärää, joka sisällytetään kysynnän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="71266-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="71266-124">Syötä Myöhästymispäivät-kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="71266-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="71266-125">Tämä on niiden päivien lukumäärä kanban-määrän laskentapäivämäärästä alkaen, joka sisällytetään kysynnän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="71266-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="71266-126">Laskennassa käytettävässä kaavassa näkyvät toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="71266-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="71266-127">Esimerkki: Kanban-määrä = ((päivän keskimääräinen kysyntä x läpimenoaika x 2,00) / tuotemäärä per käsittely-yksikkö) + 1</span><span class="sxs-lookup"><span data-stu-id="71266-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="71266-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="71266-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="71266-129">Kanban-määrän laskentakäytännön lisääminen kanban-sääntöön</span><span class="sxs-lookup"><span data-stu-id="71266-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="71266-130">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="71266-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="71266-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="71266-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71266-132">Valitse tässä menettelyssä kanban-sääntö 000020.</span><span class="sxs-lookup"><span data-stu-id="71266-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="71266-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="71266-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="71266-134">Ota käyttöön Kanban-määrän laskentakäytännöt -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="71266-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="71266-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="71266-135">Click Add.</span></span>
    * <span data-ttu-id="71266-136">Lisää edellisessä alitehtävässä luotu kanban-määrän laskentakäytäntö.</span><span class="sxs-lookup"><span data-stu-id="71266-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="71266-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="71266-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="71266-138">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="71266-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="71266-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="71266-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="71266-140">Valitse edellisessä alitehtävässä luotu käytäntö Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="71266-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

