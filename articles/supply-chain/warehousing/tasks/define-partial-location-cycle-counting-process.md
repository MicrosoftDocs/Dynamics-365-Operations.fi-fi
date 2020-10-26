---
title: Määritä sijainnin osittainen inventointiprosessi
description: Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb5c8e615302cba05fbd14a47af6578bca7bc16e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976947"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="b8311-103">Määritä sijainnin osittainen inventointiprosessi</span><span class="sxs-lookup"><span data-stu-id="b8311-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8311-104">Kun inventointisuunnitelmia käytetään inventointityön luomisessa, voit ohjata toteutuneita inventointitoimintoja pyytämällä vain tiettyjen tuotteiden ja tuotevarianttien inventointia sijainnin koko käytettävissä olevan varaston inventoinnin sijaan.</span><span class="sxs-lookup"><span data-stu-id="b8311-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="b8311-105">Tiettyjen tuotteiden suodattaminen auttaa varastopäällikköä pienentämään tarkistuksen yleiskustannuksia, estämään konsolidointivirheitä ja säästämään aikaa.</span><span class="sxs-lookup"><span data-stu-id="b8311-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="b8311-106">Yleensä nämä määritystehtävät suorittaa varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="b8311-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="b8311-107">Voit käyttää tässä menettelyssä USMF-yrityksen demotietoja tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="b8311-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="b8311-108">Inventointityömallin luominen</span><span class="sxs-lookup"><span data-stu-id="b8311-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="b8311-109">Valitse Varastonhallinta > Asetukset > Työ > Työmallit.</span><span class="sxs-lookup"><span data-stu-id="b8311-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="b8311-110">Valitse Työtilauksen tyyppi -kentässä Inventointi.</span><span class="sxs-lookup"><span data-stu-id="b8311-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="b8311-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8311-111">Click New.</span></span>
4. <span data-ttu-id="b8311-112">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b8311-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="b8311-113">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="b8311-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="b8311-114">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="b8311-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="b8311-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8311-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b8311-116">Kirjoita Työmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="b8311-117">Kirjoita Työmallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="b8311-118">Anna tai valitse Työpoolin tunnus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="b8311-119">Syötä numero Työn prioriteetti -kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8311-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="b8311-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b8311-120">Click Save.</span></span>
11. <span data-ttu-id="b8311-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8311-121">Click New.</span></span>
12. <span data-ttu-id="b8311-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8311-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b8311-123">Valitse Työtyyppi-kentässä Inventointi.</span><span class="sxs-lookup"><span data-stu-id="b8311-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="b8311-124">Syötä tai valitse arvo Työluokan tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8311-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="b8311-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b8311-125">Click Save.</span></span>
16. <span data-ttu-id="b8311-126">Valitse Työrivin tauot.</span><span class="sxs-lookup"><span data-stu-id="b8311-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="b8311-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8311-127">Click New.</span></span>
18. <span data-ttu-id="b8311-128">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b8311-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="b8311-129">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="b8311-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="b8311-130">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="b8311-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="b8311-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b8311-131">Click Save.</span></span>
20. <span data-ttu-id="b8311-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8311-132">Close the page.</span></span>
21. <span data-ttu-id="b8311-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8311-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="b8311-134">Inventointisuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="b8311-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="b8311-135">Valitse Varastonhallinta > Asetukset > Inventointi > Inventointisuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="b8311-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="b8311-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8311-136">Click New.</span></span>
3. <span data-ttu-id="b8311-137">Kirjoita Inventointisuunnitelman tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="b8311-138">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b8311-139">Lisää Inventointien enimmäismäärä -kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="b8311-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="b8311-140">Anna tai valitse Työmalli-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="b8311-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="b8311-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b8311-141">Click New.</span></span>
8. <span data-ttu-id="b8311-142">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b8311-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="b8311-143">Lajittelujärjestys on pienimmästä numerosta suurimpaan.</span><span class="sxs-lookup"><span data-stu-id="b8311-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="b8311-144">Arvon on oltava suurempi kuin 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="b8311-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="b8311-145">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8311-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b8311-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b8311-146">Click Save.</span></span>
11. <span data-ttu-id="b8311-147">Valitse Määritä tuotekysely.</span><span class="sxs-lookup"><span data-stu-id="b8311-147">Click Define product query.</span></span>
12. <span data-ttu-id="b8311-148">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b8311-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b8311-149">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b8311-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="b8311-150">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b8311-150">Click OK.</span></span>
15. <span data-ttu-id="b8311-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8311-151">Close the page.</span></span>

