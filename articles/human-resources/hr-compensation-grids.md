---
title: Kompensaatioruudukoiden määrittäminen
description: Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a66dffa26a62f2937fd54ffb175add115887398
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058941"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="ce506-103">Kompensaatioruudukoiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce506-103">Set up compensation grids</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ce506-104">Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita.</span><span class="sxs-lookup"><span data-stu-id="ce506-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="ce506-105">Kompensaatioruudukoita voidaan jakaa useiden suunnitelmien välillä tai ne voidaan kopioida uutta kompensaatiosuunnitelmaa luotaessa.</span><span class="sxs-lookup"><span data-stu-id="ce506-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="ce506-106">Tasot ja viitepisteet on määritettävä ennen kompensaatioruudukon luontia.</span><span class="sxs-lookup"><span data-stu-id="ce506-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="ce506-107">Tässä esimerkissä luodaan uusi Palkkaluokka-tyyppinen kompensaatioruudukko käyttämällä esittelytiedot tasoissa ja viitepisteissä demotietoja.</span><span class="sxs-lookup"><span data-stu-id="ce506-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="ce506-108">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ce506-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="ce506-109">Määritä kompensaatioruudukkoa koskevat tiedot</span><span class="sxs-lookup"><span data-stu-id="ce506-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="ce506-110">Valitse Henkilöstöhallinto > Kompensaatio > Kiinteä kompensaatio > Kompensaatioruudukot.</span><span class="sxs-lookup"><span data-stu-id="ce506-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="ce506-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce506-111">Click New.</span></span>
3. <span data-ttu-id="ce506-112">Kirjoita Ruudukko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="ce506-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce506-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ce506-114">Valitse vaihtoehto Tyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce506-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="ce506-115">Anna tai valitse arvo Viitemääritykset-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce506-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="ce506-116">Anna tai valitse Valuutta-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="ce506-117">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce506-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="ce506-118">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ce506-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="ce506-119">Lisää tasoja kompensaatiorakenteeseen</span><span class="sxs-lookup"><span data-stu-id="ce506-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="ce506-120">Valitse Kompensaatiorakenne.</span><span class="sxs-lookup"><span data-stu-id="ce506-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="ce506-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ce506-122">Anna tai valitse Taso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="ce506-123">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce506-123">Click New.</span></span>
5. <span data-ttu-id="ce506-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ce506-125">Anna tai valitse Taso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="ce506-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce506-126">Click New.</span></span>
8. <span data-ttu-id="ce506-127">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ce506-128">Anna tai valitse Taso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="ce506-129">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce506-129">Click New.</span></span>
11. <span data-ttu-id="ce506-130">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="ce506-131">Anna tai valitse Taso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="ce506-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ce506-132">Click New.</span></span>
14. <span data-ttu-id="ce506-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="ce506-134">Anna tai valitse Taso-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="ce506-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="ce506-135">Täytä kompensaatiorakenteen arvot</span><span class="sxs-lookup"><span data-stu-id="ce506-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="ce506-136">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ce506-137">Kompensaatioarvot voidaan lisätä tässä vaiheessa taulun kenttiin. Joukkomuutos-toiminnolla voidaan vaihtoehtoisesti täyttää kätevästi useita kenttiä ja suorittaa peruslaskutoimituksia.</span><span class="sxs-lookup"><span data-stu-id="ce506-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="ce506-138">Valitse Joukkomuutos.</span><span class="sxs-lookup"><span data-stu-id="ce506-138">Click Mass change.</span></span>
    * <span data-ttu-id="ce506-139">Tässä ruudukossa käytetään ensiksi ensimmäisen tason keskipisteen arvoa kaikkiin taulun kenttiin.</span><span class="sxs-lookup"><span data-stu-id="ce506-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="ce506-140">Kompensaatiomatriisi tulee perustumaan siihen.</span><span class="sxs-lookup"><span data-stu-id="ce506-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="ce506-141">Valitse Oikaisulaji-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ce506-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="ce506-142">Syötä Oikaisusumma-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce506-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="ce506-143">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="ce506-144">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="ce506-145">Seuraavaksi kasvatetaan joukkomuutostoiminnolla kunkin seuraavan tason summia tietyllä prosentilla tai summalla.</span><span class="sxs-lookup"><span data-stu-id="ce506-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="ce506-146">Tässä esimerkissä jokaisella luokalla on 12,5 prosentin hajonta keskipisteiden välillä.</span><span class="sxs-lookup"><span data-stu-id="ce506-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="ce506-147">Valitse Oikaisulaji-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ce506-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="ce506-148">Syötä Oikaisusumma-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce506-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="ce506-149">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ce506-150">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ce506-151">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ce506-152">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ce506-153">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="ce506-154">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ce506-155">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ce506-156">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ce506-157">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="ce506-158">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="ce506-159">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="ce506-160">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="ce506-161">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ce506-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="ce506-162">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="ce506-163">Nyt joukkomuutostoiminnolla muutetaan kunkin tason pienintä ja suurinta viitepistettä.</span><span class="sxs-lookup"><span data-stu-id="ce506-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="ce506-164">Tässä esimerkissä käytetään 50 prosentin hajontaa, joten pienintä viitepistettä vähennetään 20 prosentilla ja suurinta suurennetaan 20 prosentilla.</span><span class="sxs-lookup"><span data-stu-id="ce506-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="ce506-165">Syötä Oikaisusumma-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce506-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="ce506-166">Anna tai valitse arvo Viitepiste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce506-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="ce506-167">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="ce506-168">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="ce506-169">Syötä Oikaisusumma-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ce506-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="ce506-170">Anna tai valitse arvo Viitepiste-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ce506-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="ce506-171">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ce506-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="ce506-172">Valitse Sovella ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="ce506-172">Click Apply to grid.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]