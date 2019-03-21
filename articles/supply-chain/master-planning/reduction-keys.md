---
title: Vähennysavaimet
description: Tämä artikkeli sisältää esimerkkejä, jotka kuvaavat vähennysavaimen määrittämistä. Artikkelissa kuvataan erilaisia vähennysavaimen asetuksia ja kunkin asetuksen tuloksia. Vähennysavaimen avulla voit määrittää, kuinka ennustevaatimuksia voidaan vähentää.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2019
ms.locfileid: "770913"
---
# <a name="reduction-keys"></a><span data-ttu-id="17e4c-105">Vähennysavaimet</span><span class="sxs-lookup"><span data-stu-id="17e4c-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17e4c-106">Tämä artikkeli sisältää esimerkkejä, jotka kuvaavat vähennysavaimen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="17e4c-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="17e4c-107">Artikkelissa kuvataan erilaisia vähennysavaimen asetuksia ja kunkin asetuksen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="17e4c-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="17e4c-108">Vähennysavaimen avulla voit määrittää, kuinka ennustevaatimuksia voidaan vähentää.</span><span class="sxs-lookup"><span data-stu-id="17e4c-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="17e4c-109">Esimerkki 1: Ennusteen vähennysperiaatteena Prosentti – vähennysavain</span><span class="sxs-lookup"><span data-stu-id="17e4c-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="17e4c-110">Tämä esimerkki osoittaa, miten vähennysavain pienentää kysynnän ennustetarpeita vähennysavaimen määrittämien prosenttien ja kausien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="17e4c-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="17e4c-111">Määritä **Vähennysavaimet**-sivulla seuraavat rivit.</span><span class="sxs-lookup"><span data-stu-id="17e4c-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="17e4c-112">Vaihto</span><span class="sxs-lookup"><span data-stu-id="17e4c-112">Change</span></span> | <span data-ttu-id="17e4c-113">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="17e4c-113">Unit</span></span>  | <span data-ttu-id="17e4c-114">Prosentti</span><span class="sxs-lookup"><span data-stu-id="17e4c-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="17e4c-115">1</span><span class="sxs-lookup"><span data-stu-id="17e4c-115">1</span></span>    | <span data-ttu-id="17e4c-116">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-116">Month</span></span> |   <span data-ttu-id="17e4c-117">100</span><span class="sxs-lookup"><span data-stu-id="17e4c-117">100</span></span>   |
   |   <span data-ttu-id="17e4c-118">2</span><span class="sxs-lookup"><span data-stu-id="17e4c-118">2</span></span>    | <span data-ttu-id="17e4c-119">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-119">Month</span></span> |   <span data-ttu-id="17e4c-120">75</span><span class="sxs-lookup"><span data-stu-id="17e4c-120">75</span></span>    |
   |   <span data-ttu-id="17e4c-121">3</span><span class="sxs-lookup"><span data-stu-id="17e4c-121">3</span></span>    | <span data-ttu-id="17e4c-122">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-122">Month</span></span> |   <span data-ttu-id="17e4c-123">50</span><span class="sxs-lookup"><span data-stu-id="17e4c-123">50</span></span>    |
   |   <span data-ttu-id="17e4c-124">4</span><span class="sxs-lookup"><span data-stu-id="17e4c-124">4</span></span>    | <span data-ttu-id="17e4c-125">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-125">Month</span></span> |   <span data-ttu-id="17e4c-126">25</span><span class="sxs-lookup"><span data-stu-id="17e4c-126">25</span></span>    |


2. <span data-ttu-id="17e4c-127">Linkitä vähennysavain nimikkeen kattavuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="17e4c-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="17e4c-128">Valitse **Pääsuunnitelmat**-sivulla **Vähennysperiaate** -kentästä **Prosentti - vähennysavain**.</span><span class="sxs-lookup"><span data-stu-id="17e4c-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="17e4c-129">Luo kysynnän ennuste 1 000 kappaleesta kuukaudessa.</span><span class="sxs-lookup"><span data-stu-id="17e4c-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="17e4c-130">Jos suoritat ennusteajoituksen 1. tammikuuta, kysynnän ennustetarpeita kulutetaan **Vähennysavaimet**-sivulla määritettyjen prosenttien mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="17e4c-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="17e4c-131">Pääsuunnitelmaan siirretään seuraavat tarvemäärät.</span><span class="sxs-lookup"><span data-stu-id="17e4c-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="17e4c-132">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-132">Month</span></span>                | <span data-ttu-id="17e4c-133">Kappaletarve</span><span class="sxs-lookup"><span data-stu-id="17e4c-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="17e4c-134">Tammikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-134">January</span></span>              | <span data-ttu-id="17e4c-135">0</span><span class="sxs-lookup"><span data-stu-id="17e4c-135">0</span></span>                         |
| <span data-ttu-id="17e4c-136">Helmikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-136">February</span></span>             | <span data-ttu-id="17e4c-137">250</span><span class="sxs-lookup"><span data-stu-id="17e4c-137">250</span></span>                       |
| <span data-ttu-id="17e4c-138">Maaliskuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-138">March</span></span>                | <span data-ttu-id="17e4c-139">500</span><span class="sxs-lookup"><span data-stu-id="17e4c-139">500</span></span>                       |
| <span data-ttu-id="17e4c-140">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-140">April</span></span>                | <span data-ttu-id="17e4c-141">750</span><span class="sxs-lookup"><span data-stu-id="17e4c-141">750</span></span>                       |
| <span data-ttu-id="17e4c-142">Touko–joulukuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-142">May through December</span></span> | <span data-ttu-id="17e4c-143">1 000</span><span class="sxs-lookup"><span data-stu-id="17e4c-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="17e4c-144">Esimerkki 2: Ennusteen vähennysperiaatteena Tapahtumat – vähennysavain</span><span class="sxs-lookup"><span data-stu-id="17e4c-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="17e4c-145">Tämä esimerkki osoittaa, miten vähennysavaimen määrittelemillä jaksoilla toteutuvat tilaukset pienentävät kysynnän ennustetarpeita.</span><span class="sxs-lookup"><span data-stu-id="17e4c-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="17e4c-146">Valitse **Pääsuunnitelmat**-sivulla **Vähennysperiaate** -kentästä **Tapahtuma - vähennysavain**.</span><span class="sxs-lookup"><span data-stu-id="17e4c-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="17e4c-147">1. tammikuuta mennessä on tehty seuraavat myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="17e4c-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="17e4c-148">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-148">Month</span></span>    | <span data-ttu-id="17e4c-149">Tilattu kappalemäärä</span><span class="sxs-lookup"><span data-stu-id="17e4c-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="17e4c-150">Tammikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-150">January</span></span>  | <span data-ttu-id="17e4c-151">956</span><span class="sxs-lookup"><span data-stu-id="17e4c-151">956</span></span>                      |
| <span data-ttu-id="17e4c-152">Helmikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-152">February</span></span> | <span data-ttu-id="17e4c-153">1 176</span><span class="sxs-lookup"><span data-stu-id="17e4c-153">1,176</span></span>                    |
| <span data-ttu-id="17e4c-154">Maaliskuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-154">March</span></span>    | <span data-ttu-id="17e4c-155">451</span><span class="sxs-lookup"><span data-stu-id="17e4c-155">451</span></span>                      |
| <span data-ttu-id="17e4c-156">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-156">April</span></span>    | <span data-ttu-id="17e4c-157">119</span><span class="sxs-lookup"><span data-stu-id="17e4c-157">119</span></span>                      |

<span data-ttu-id="17e4c-158">Jos käytät samaa 1 000 kappaleen kysyntäennustetta kuukaudessa, pääsuunnitelmaan siirretään seuraavat tarvemäärät.</span><span class="sxs-lookup"><span data-stu-id="17e4c-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="17e4c-159">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-159">Month</span></span>                | <span data-ttu-id="17e4c-160">Kappaletarve</span><span class="sxs-lookup"><span data-stu-id="17e4c-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="17e4c-161">Tammikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-161">January</span></span>              | <span data-ttu-id="17e4c-162">44</span><span class="sxs-lookup"><span data-stu-id="17e4c-162">44</span></span>                        |
| <span data-ttu-id="17e4c-163">Helmikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-163">February</span></span>             | <span data-ttu-id="17e4c-164">0</span><span class="sxs-lookup"><span data-stu-id="17e4c-164">0</span></span>                         |
| <span data-ttu-id="17e4c-165">Maaliskuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-165">March</span></span>                | <span data-ttu-id="17e4c-166">549</span><span class="sxs-lookup"><span data-stu-id="17e4c-166">549</span></span>                       |
| <span data-ttu-id="17e4c-167">Huhtikuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-167">April</span></span>                | <span data-ttu-id="17e4c-168">881</span><span class="sxs-lookup"><span data-stu-id="17e4c-168">881</span></span>                       |
| <span data-ttu-id="17e4c-169">Touko–joulukuu</span><span class="sxs-lookup"><span data-stu-id="17e4c-169">May through December</span></span> | <span data-ttu-id="17e4c-170">1 000</span><span class="sxs-lookup"><span data-stu-id="17e4c-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="17e4c-171">Esimerkki 3: Ennusteen vähennysperiaatteena Tapahtumat – dynaaminen kausi</span><span class="sxs-lookup"><span data-stu-id="17e4c-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="17e4c-172">Useimmiten järjestelmät on määritetty siten, että tapahtumat vähentävät kysynnän ennustetta määritetyillä ennustekausilla: viikkoina, kuukausina ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="17e4c-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="17e4c-173">Nämä kaudet vähennysavaimeen.</span><span class="sxs-lookup"><span data-stu-id="17e4c-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="17e4c-174">Kahden kysynnän ennusterivin välinen aika voi kuitenkin myös *vihjata* tiettyyn kauteen.</span><span class="sxs-lookup"><span data-stu-id="17e4c-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="17e4c-175">Luo kysynnän ennuste seuraaville päivämäärille ja määrille.</span><span class="sxs-lookup"><span data-stu-id="17e4c-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="17e4c-176">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="17e4c-176">Date</span></span>       | <span data-ttu-id="17e4c-177">Kysynnän ennuste</span><span class="sxs-lookup"><span data-stu-id="17e4c-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="17e4c-178">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-178">January 1</span></span>  | <span data-ttu-id="17e4c-179">1 000</span><span class="sxs-lookup"><span data-stu-id="17e4c-179">1,000</span></span>           |
   | <span data-ttu-id="17e4c-180">5. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-180">January 5</span></span>  | <span data-ttu-id="17e4c-181">500</span><span class="sxs-lookup"><span data-stu-id="17e4c-181">500</span></span>             |
   | <span data-ttu-id="17e4c-182">12. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-182">January 12</span></span> | <span data-ttu-id="17e4c-183">1 000</span><span class="sxs-lookup"><span data-stu-id="17e4c-183">1,000</span></span>           |

   <span data-ttu-id="17e4c-184">Tässä ennusteessa ennustepäivämäärien välillä ei ole selvää jaksoa. Ensimmäisen ja toisen päivämäärän välissä on neljä päivää ja toisen sekä kolmannen päivämäärän välissä seitsemän päivää.</span><span class="sxs-lookup"><span data-stu-id="17e4c-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="17e4c-185">Nämä eri aikavälit ovat dynaamisia kausia.</span><span class="sxs-lookup"><span data-stu-id="17e4c-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="17e4c-186">Luo myyntitilausrivit seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="17e4c-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="17e4c-187">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="17e4c-187">Date</span></span>                             | <span data-ttu-id="17e4c-188">Myyntitilauksen määrä</span><span class="sxs-lookup"><span data-stu-id="17e4c-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="17e4c-189">15. joulukuuta edellisenä vuonna</span><span class="sxs-lookup"><span data-stu-id="17e4c-189">December 15 in the previous year</span></span> | <span data-ttu-id="17e4c-190">500</span><span class="sxs-lookup"><span data-stu-id="17e4c-190">500</span></span>                  |
   | <span data-ttu-id="17e4c-191">3. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-191">January 3</span></span>                        | <span data-ttu-id="17e4c-192">100</span><span class="sxs-lookup"><span data-stu-id="17e4c-192">100</span></span>                  |
   | <span data-ttu-id="17e4c-193">10. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-193">January 10</span></span>                       | <span data-ttu-id="17e4c-194">200</span><span class="sxs-lookup"><span data-stu-id="17e4c-194">200</span></span>                  |

<span data-ttu-id="17e4c-195">Ennustetta vähennetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="17e4c-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="17e4c-196">Ensimmäinen myyntitilaus ei ole millään kaudella, joten se ei vähennä mitään ennustetta.</span><span class="sxs-lookup"><span data-stu-id="17e4c-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="17e4c-197">Toinen myyntitilaus on 1.–5. tammikuuta, joten se vähentää tammikuun 1. päivän ennustetta 100:lla.</span><span class="sxs-lookup"><span data-stu-id="17e4c-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="17e4c-198">Kolmas myyntitilaus on 5.–12. tammikuuta, joten se vähentää tammikuun 5. päivän 200:lla.</span><span class="sxs-lookup"><span data-stu-id="17e4c-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="17e4c-199">Ennusteen täyttämiseksi luodaan seuraava suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="17e4c-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="17e4c-200">Kysynnän ennusteen päivämäärä</span><span class="sxs-lookup"><span data-stu-id="17e4c-200">Demand forecast date</span></span> | <span data-ttu-id="17e4c-201">Vähennetty määrä</span><span class="sxs-lookup"><span data-stu-id="17e4c-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="17e4c-202">1. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-202">January 1</span></span>            | <span data-ttu-id="17e4c-203">900</span><span class="sxs-lookup"><span data-stu-id="17e4c-203">900</span></span>              |
| <span data-ttu-id="17e4c-204">5. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-204">January 5</span></span>            | <span data-ttu-id="17e4c-205">300</span><span class="sxs-lookup"><span data-stu-id="17e4c-205">300</span></span>              |
| <span data-ttu-id="17e4c-206">12. tammikuuta</span><span class="sxs-lookup"><span data-stu-id="17e4c-206">January 12</span></span>           | <span data-ttu-id="17e4c-207">1 000</span><span class="sxs-lookup"><span data-stu-id="17e4c-207">1,000</span></span>            |

<span data-ttu-id="17e4c-208">Seuraavassa on yhteenveto **Tapahtumat - dynaaminen kausi** -vähennyksestä:</span><span class="sxs-lookup"><span data-stu-id="17e4c-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="17e4c-209">Ennustetarvetta vähentävät dynaamisella kaudella tapahtuvat toteutuneet tilaustapahtumat</span><span class="sxs-lookup"><span data-stu-id="17e4c-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="17e4c-210">Dynaaminen kausi kattaa nykyiset ennustepäivämäärät ja päättyy seuraavan ennusteen alkuun.</span><span class="sxs-lookup"><span data-stu-id="17e4c-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="17e4c-211">Tämä menetelmä ei käytä tai edellytä vähennysavainta.</span><span class="sxs-lookup"><span data-stu-id="17e4c-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="17e4c-212">Kun tätä vaihtoehtoa käytetään, tapahtuu seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="17e4c-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="17e4c-213">Jos ennuste vähenee kokonaan, nykyisen ennusteen ennustetarpeiksi tulee nolla.</span><span class="sxs-lookup"><span data-stu-id="17e4c-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="17e4c-214">Jos tulevaa ennustetta ei ole, vähennetään edellisen syötetyn ennusteen ennustetarpeita.</span><span class="sxs-lookup"><span data-stu-id="17e4c-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="17e4c-215">Ennusteen vähennyslaskentaan sisällytetään aikarajat.</span><span class="sxs-lookup"><span data-stu-id="17e4c-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="17e4c-216">Ennusteen vähennyslaskentaan sisällytetään positiiviset päivät.</span><span class="sxs-lookup"><span data-stu-id="17e4c-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="17e4c-217">Jos toteutuneet tilaustapahtumat ylittävät ennustetarpeet, jäljelle jääviä tapahtumia ei siirretä seuraavalle ennustekaudelle.</span><span class="sxs-lookup"><span data-stu-id="17e4c-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="17e4c-218">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="17e4c-218">Additional resources</span></span>
--------

[<span data-ttu-id="17e4c-219">Pääsuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="17e4c-219">Master plans</span></span>](master-plans.md)



