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
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab17ba5a6ee950c2d3977990123a8f9277f858ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998808"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="3a5dc-103">Lisää kanban-määrän laskentakäytäntö kanban-sääntöön</span><span class="sxs-lookup"><span data-stu-id="3a5dc-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a5dc-104">Tässä menettelyssä keskitytään kanban-määrän laskentakäytännön luomiseen ja sen lisäämiseen kanban-sääntöön kanbanin koon ja määrien optimoimista varten.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="3a5dc-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3a5dc-106">Tämä menettely on tarkoitettu arvovirtaa hallitsevalle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="3a5dc-107">Tämä menettely on Laske kanban-määräehdotukset -menettelyn luomisen edellytys.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="3a5dc-108">Uuden kanban-määrän laskentakäytännön luominen</span><span class="sxs-lookup"><span data-stu-id="3a5dc-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="3a5dc-109">Siirry kohtaan Tuotannonhallinta > Kausittaiset tehtävät > Kanban-määrän laskeminen > Kanban-määrän laskentakäytännöt.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="3a5dc-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-110">Click New.</span></span>
3. <span data-ttu-id="3a5dc-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3a5dc-112">Syötä esimerkiksi arvo Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="3a5dc-113">Avaa haku valitsemalla Pääsuunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3a5dc-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a5dc-115">Valitse StaticPlan, kun haluat laskea kysynnän.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="3a5dc-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3a5dc-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-117">Click Save.</span></span>
8. <span data-ttu-id="3a5dc-118">Syötä Kanban-määrä vähintään -kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="3a5dc-119">Tämä on kanbanien lisänumero, joka sisällytetään kanban-määrän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="3a5dc-120">Määritä turvallisuuskertoimeksi 1.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="3a5dc-121">Tämä on kerroin, jota käytetään varmuusvaraston lisämäärän laskennassa.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="3a5dc-122">Syötä Jäljellä olevat päivät -kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="3a5dc-123">Tämä on niiden päivien lukumäärä ennen kanban-määrän laskentapäivämäärää, joka sisällytetään kysynnän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="3a5dc-124">Syötä Myöhästymispäivät-kenttään 30.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="3a5dc-125">Tämä on niiden päivien lukumäärä kanban-määrän laskentapäivämäärästä alkaen, joka sisällytetään kysynnän laskentaan.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="3a5dc-126">Laskennassa käytettävässä kaavassa näkyvät toteutuneet arvot.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="3a5dc-127">Esimerkki: Kanban-määrä = ((päivän keskimääräinen kysyntä x läpimenoaika x 2,00) / tuotemäärä per käsittely-yksikkö) + 1</span><span class="sxs-lookup"><span data-stu-id="3a5dc-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="3a5dc-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="3a5dc-129">Kanban-määrän laskentakäytännön lisääminen kanban-sääntöön</span><span class="sxs-lookup"><span data-stu-id="3a5dc-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="3a5dc-130">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3a5dc-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a5dc-132">Valitse tässä menettelyssä kanban-sääntö 000020.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="3a5dc-133">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3a5dc-134">Ota käyttöön Kanban-määrän laskentakäytännöt -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="3a5dc-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-135">Click Add.</span></span>
    * <span data-ttu-id="3a5dc-136">Lisää edellisessä alitehtävässä luotu kanban-määrän laskentakäytäntö.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="3a5dc-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3a5dc-138">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3a5dc-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3a5dc-140">Valitse edellisessä alitehtävässä luotu käytäntö Kaiutin2016.</span><span class="sxs-lookup"><span data-stu-id="3a5dc-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

