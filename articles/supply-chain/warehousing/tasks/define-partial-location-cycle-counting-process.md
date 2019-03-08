---
title: Määritä sijainnin osittainen inventointiprosessi
description: Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2019
ms.locfileid: "373396"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="c38d2-103">Määritä sijainnin osittainen inventointiprosessi</span><span class="sxs-lookup"><span data-stu-id="c38d2-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c38d2-104">Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan.</span><span class="sxs-lookup"><span data-stu-id="c38d2-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="c38d2-105">Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, estämään konsolidointivirheitä ja säästämään aikaa.</span><span class="sxs-lookup"><span data-stu-id="c38d2-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="c38d2-106">Yleensä nämä määritystehtävät suorittaa varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="c38d2-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="c38d2-107">Voit käyttää tässä menettelyssä USMF-yrityksen demotietoja tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="c38d2-108">Inventointityömallin luominen</span><span class="sxs-lookup"><span data-stu-id="c38d2-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="c38d2-109">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="c38d2-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="c38d2-110">Valitse Työtilauksen tyyppi -kentässä Inventointi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="c38d2-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-111">Click New.</span></span>
4. <span data-ttu-id="c38d2-112">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c38d2-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="c38d2-113">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="c38d2-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="c38d2-114">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="c38d2-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="c38d2-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c38d2-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c38d2-116">Kirjoita Työmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="c38d2-117">Kirjoita Työmallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="c38d2-118">Anna tai valitse Työpoolin tunnus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="c38d2-119">Syötä numero Työn prioriteetti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c38d2-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="c38d2-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c38d2-120">Click Save.</span></span>
11. <span data-ttu-id="c38d2-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-121">Click New.</span></span>
12. <span data-ttu-id="c38d2-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c38d2-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c38d2-123">Valitse Työtyyppi-kentässä Inventointi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="c38d2-124">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c38d2-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="c38d2-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c38d2-125">Click Save.</span></span>
16. <span data-ttu-id="c38d2-126">Valitse Työrivin tauot.</span><span class="sxs-lookup"><span data-stu-id="c38d2-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="c38d2-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-127">Click New.</span></span>
18. <span data-ttu-id="c38d2-128">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c38d2-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="c38d2-129">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="c38d2-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="c38d2-130">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="c38d2-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="c38d2-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c38d2-131">Click Save.</span></span>
20. <span data-ttu-id="c38d2-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c38d2-132">Close the page.</span></span>
21. <span data-ttu-id="c38d2-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c38d2-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="c38d2-134">Inventointisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="c38d2-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="c38d2-135">Valitse Varastonhallinta > Asetukset > Inventointi > Inventointisuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="c38d2-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="c38d2-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-136">Click New.</span></span>
3. <span data-ttu-id="c38d2-137">Kirjoita Inventointisuunnitelman tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="c38d2-138">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c38d2-139">Lisää Inventointien enimmäismäärä -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="c38d2-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="c38d2-140">Anna tai valitse Työmalli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="c38d2-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="c38d2-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c38d2-141">Click New.</span></span>
8. <span data-ttu-id="c38d2-142">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c38d2-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="c38d2-143">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="c38d2-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="c38d2-144">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="c38d2-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="c38d2-145">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c38d2-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c38d2-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c38d2-146">Click Save.</span></span>
11. <span data-ttu-id="c38d2-147">Valitse Määritä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="c38d2-147">Click Define product query.</span></span>
12. <span data-ttu-id="c38d2-148">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c38d2-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c38d2-149">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c38d2-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="c38d2-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c38d2-150">Click OK.</span></span>
15. <span data-ttu-id="c38d2-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c38d2-151">Close the page.</span></span>

