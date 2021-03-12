---
title: Varaston erääntymisraporttien esimerkkejä ja logiikka
description: Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan varaston erääntymisraportin tuloksia.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983922"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="52903-103">Varaston erääntymisraporttien esimerkkejä ja logiikka</span><span class="sxs-lookup"><span data-stu-id="52903-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52903-104">Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan **Varaston erääntyminen** -raportin tuloksia.</span><span class="sxs-lookup"><span data-stu-id="52903-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="52903-105">Tämä raportti luokittelee valitun nimikkeen tai nimikeryhmän varastosaldon ja varastoarvot useisiin aikaväleihin.</span><span class="sxs-lookup"><span data-stu-id="52903-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="52903-106">Ohjeaiheessa myös näytetään raportin sisäinen logiikka.</span><span class="sxs-lookup"><span data-stu-id="52903-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="52903-107">Ohjeaiheen esimerkeissä näytetään tulokset, jotka esitetään **Varaston erääntyminen** -vakioraportissa.</span><span class="sxs-lookup"><span data-stu-id="52903-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="52903-108">Yleensä kannattaa kuitenkin käyttää tämän raportin [Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md) -versiota, etenkin jos käsiteltäviä nimikkeitä ja varastoja on paljon.</span><span class="sxs-lookup"><span data-stu-id="52903-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="52903-109">Varaston erääntymisraportin tallennus tallentaa jokaisen luodun raportin, näyttää tulokset vuorovaikutteisena sivuna ja kaaviona sekä sallii minkä tahansa tallennetun raportin viennin.</span><span class="sxs-lookup"><span data-stu-id="52903-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="52903-110">Esimerkeissä käytettävät mallitiedot</span><span class="sxs-lookup"><span data-stu-id="52903-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="52903-111">Ohjeaiheen esimerkit perustuvat tässä osassa käsiteltäviin varastotapahtuman mallitietoihin.</span><span class="sxs-lookup"><span data-stu-id="52903-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="52903-112">Varastodimensioryhmän määritys</span><span class="sxs-lookup"><span data-stu-id="52903-112">Storage dimension setup</span></span>

<span data-ttu-id="52903-113">Esimerkkijärjestelmässä on seuraavat varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="52903-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="52903-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="52903-114">Name</span></span>      | <span data-ttu-id="52903-115">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="52903-115">Active</span></span> | <span data-ttu-id="52903-116">Fyysinen varasto</span><span class="sxs-lookup"><span data-stu-id="52903-116">Physical inventory</span></span> | <span data-ttu-id="52903-117">Kirjanpitovarasto</span><span class="sxs-lookup"><span data-stu-id="52903-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="52903-118">Sivusto</span><span class="sxs-lookup"><span data-stu-id="52903-118">Site</span></span>      | <span data-ttu-id="52903-119">Kyllä</span><span class="sxs-lookup"><span data-stu-id="52903-119">Yes</span></span>    | <span data-ttu-id="52903-120">Kyllä</span><span class="sxs-lookup"><span data-stu-id="52903-120">Yes</span></span>                | <span data-ttu-id="52903-121">Kyllä</span><span class="sxs-lookup"><span data-stu-id="52903-121">Yes</span></span>                 |
| <span data-ttu-id="52903-122">Varasto</span><span class="sxs-lookup"><span data-stu-id="52903-122">Warehouse</span></span> | <span data-ttu-id="52903-123">Kyllä</span><span class="sxs-lookup"><span data-stu-id="52903-123">Yes</span></span>    | <span data-ttu-id="52903-124">Kyllä</span><span class="sxs-lookup"><span data-stu-id="52903-124">Yes</span></span>                | <span data-ttu-id="52903-125">Nro</span><span class="sxs-lookup"><span data-stu-id="52903-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="52903-126">Varastomalli</span><span class="sxs-lookup"><span data-stu-id="52903-126">Inventory model</span></span>

<span data-ttu-id="52903-127">Esimerkkijärjestelmän vapautettujen tuotteiden varastomallin on *FIFO* ja varastomallin **Kustannushinta**-asetus on *Sisällytä fyysinen arvo*.</span><span class="sxs-lookup"><span data-stu-id="52903-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="52903-128">Varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="52903-128">Inventory transactions</span></span>

<span data-ttu-id="52903-129">Esimerkkijärjestelmä sisältää seuraavat vapautetun tuotteen varastotapahtumat, kun tuotteen nimikenumero on *1000*.</span><span class="sxs-lookup"><span data-stu-id="52903-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="52903-130">Viite</span><span class="sxs-lookup"><span data-stu-id="52903-130">Reference</span></span>      | <span data-ttu-id="52903-131">Sivusto</span><span class="sxs-lookup"><span data-stu-id="52903-131">Site</span></span> | <span data-ttu-id="52903-132">Varasto</span><span class="sxs-lookup"><span data-stu-id="52903-132">Warehouse</span></span> | <span data-ttu-id="52903-133">Kuitti</span><span class="sxs-lookup"><span data-stu-id="52903-133">Receipt</span></span>   | <span data-ttu-id="52903-134">Otto</span><span class="sxs-lookup"><span data-stu-id="52903-134">Issue</span></span> | <span data-ttu-id="52903-135">Fyysinen pvm.</span><span class="sxs-lookup"><span data-stu-id="52903-135">Physical date</span></span> | <span data-ttu-id="52903-136">Rahoituspvm.</span><span class="sxs-lookup"><span data-stu-id="52903-136">Financial date</span></span> | <span data-ttu-id="52903-137">Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-137">Quantity</span></span> | <span data-ttu-id="52903-138">Kustannussumma</span><span class="sxs-lookup"><span data-stu-id="52903-138">Cost amount</span></span> | <span data-ttu-id="52903-139">Fyysinen kustannus</span><span class="sxs-lookup"><span data-stu-id="52903-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="52903-140">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="52903-140">Purchase order</span></span> | <span data-ttu-id="52903-141">1</span><span class="sxs-lookup"><span data-stu-id="52903-141">1</span></span>    | <span data-ttu-id="52903-142">11</span><span class="sxs-lookup"><span data-stu-id="52903-142">11</span></span>        | <span data-ttu-id="52903-143">Ostettu</span><span class="sxs-lookup"><span data-stu-id="52903-143">Purchased</span></span> |       | <span data-ttu-id="52903-144">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="52903-144">March 15</span></span>      | <span data-ttu-id="52903-145">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="52903-145">March 15</span></span>       | <span data-ttu-id="52903-146">10</span><span class="sxs-lookup"><span data-stu-id="52903-146">10</span></span>       | <span data-ttu-id="52903-147">1 000</span><span class="sxs-lookup"><span data-stu-id="52903-147">1,000</span></span>       | <span data-ttu-id="52903-148">1 000</span><span class="sxs-lookup"><span data-stu-id="52903-148">1,000</span></span>                |
| <span data-ttu-id="52903-149">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="52903-149">Purchase order</span></span> | <span data-ttu-id="52903-150">2</span><span class="sxs-lookup"><span data-stu-id="52903-150">2</span></span>    | <span data-ttu-id="52903-151">21</span><span class="sxs-lookup"><span data-stu-id="52903-151">21</span></span>        | <span data-ttu-id="52903-152">Ostettu</span><span class="sxs-lookup"><span data-stu-id="52903-152">Purchased</span></span> |       | <span data-ttu-id="52903-153">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="52903-153">March 15</span></span>      | <span data-ttu-id="52903-154">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="52903-154">March 15</span></span>       | <span data-ttu-id="52903-155">10</span><span class="sxs-lookup"><span data-stu-id="52903-155">10</span></span>       | <span data-ttu-id="52903-156">2,000</span><span class="sxs-lookup"><span data-stu-id="52903-156">2,000</span></span>       | <span data-ttu-id="52903-157">2,000</span><span class="sxs-lookup"><span data-stu-id="52903-157">2,000</span></span>                |
| <span data-ttu-id="52903-158">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="52903-158">Purchase order</span></span> | <span data-ttu-id="52903-159">1</span><span class="sxs-lookup"><span data-stu-id="52903-159">1</span></span>    | <span data-ttu-id="52903-160">11</span><span class="sxs-lookup"><span data-stu-id="52903-160">11</span></span>        | <span data-ttu-id="52903-161">Vastaanotettu</span><span class="sxs-lookup"><span data-stu-id="52903-161">Received</span></span>  |       | <span data-ttu-id="52903-162">Huhtikuun 15.</span><span class="sxs-lookup"><span data-stu-id="52903-162">April 15</span></span>      |                | <span data-ttu-id="52903-163">5</span><span class="sxs-lookup"><span data-stu-id="52903-163">5</span></span>        |             | <span data-ttu-id="52903-164">375</span><span class="sxs-lookup"><span data-stu-id="52903-164">375</span></span>                  |
| <span data-ttu-id="52903-165">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="52903-165">Transfer order</span></span> | <span data-ttu-id="52903-166">1</span><span class="sxs-lookup"><span data-stu-id="52903-166">1</span></span>    | <span data-ttu-id="52903-167">11</span><span class="sxs-lookup"><span data-stu-id="52903-167">11</span></span>        |           | <span data-ttu-id="52903-168">Myyty</span><span class="sxs-lookup"><span data-stu-id="52903-168">Sold</span></span>  | <span data-ttu-id="52903-169">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="52903-169">May 2</span></span>         | <span data-ttu-id="52903-170">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="52903-170">May 2</span></span>          | <span data-ttu-id="52903-171">-5</span><span class="sxs-lookup"><span data-stu-id="52903-171">-5</span></span>       | <span data-ttu-id="52903-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="52903-172">-458.33</span></span>     | <span data-ttu-id="52903-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="52903-173">-458.33</span></span>              |
| <span data-ttu-id="52903-174">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="52903-174">Transfer order</span></span> | <span data-ttu-id="52903-175">1</span><span class="sxs-lookup"><span data-stu-id="52903-175">1</span></span>    | <span data-ttu-id="52903-176">12</span><span class="sxs-lookup"><span data-stu-id="52903-176">12</span></span>        | <span data-ttu-id="52903-177">Ostettu</span><span class="sxs-lookup"><span data-stu-id="52903-177">Purchased</span></span> |       | <span data-ttu-id="52903-178">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="52903-178">May 2</span></span>         | <span data-ttu-id="52903-179">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="52903-179">May 2</span></span>          | <span data-ttu-id="52903-180">5</span><span class="sxs-lookup"><span data-stu-id="52903-180">5</span></span>        | <span data-ttu-id="52903-181">458.33</span><span class="sxs-lookup"><span data-stu-id="52903-181">458.33</span></span>      | <span data-ttu-id="52903-182">458.33</span><span class="sxs-lookup"><span data-stu-id="52903-182">458.33</span></span>               |
| <span data-ttu-id="52903-183">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="52903-183">Sales order</span></span>    | <span data-ttu-id="52903-184">1</span><span class="sxs-lookup"><span data-stu-id="52903-184">1</span></span>    | <span data-ttu-id="52903-185">12</span><span class="sxs-lookup"><span data-stu-id="52903-185">12</span></span>        |           | <span data-ttu-id="52903-186">Myyty</span><span class="sxs-lookup"><span data-stu-id="52903-186">Sold</span></span>  | <span data-ttu-id="52903-187">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="52903-187">May 3</span></span>         | <span data-ttu-id="52903-188">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="52903-188">May 3</span></span>          | <span data-ttu-id="52903-189">-1</span><span class="sxs-lookup"><span data-stu-id="52903-189">-1</span></span>       | <span data-ttu-id="52903-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="52903-190">-91.67</span></span>      | <span data-ttu-id="52903-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="52903-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="52903-192">Kunkin aikavälin määrien ja summien laskeminen</span><span class="sxs-lookup"><span data-stu-id="52903-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="52903-193">Edellisissä osissa kuvattuja mallitietoja käyttämällä voit suorittaa **Varaston erääntyminen** -raportin, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="52903-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="52903-194">**Alkupäivämäärä:** *9.5.2020*</span><span class="sxs-lookup"><span data-stu-id="52903-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="52903-195">**Paikka:** *Näkymä*</span><span class="sxs-lookup"><span data-stu-id="52903-195">**Site:** *View*</span></span>
- <span data-ttu-id="52903-196">**Varasto**: *Ei*</span><span class="sxs-lookup"><span data-stu-id="52903-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="52903-197">**Nimiketunnus:** *Yhteensä*</span><span class="sxs-lookup"><span data-stu-id="52903-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="52903-198">**Erääntymiskausi:** Tämän kentän käyttäminen luo kuukausittaiset aikavälit.</span><span class="sxs-lookup"><span data-stu-id="52903-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="52903-199">Tässä tapauksessa luotu luodun raportin sisältö muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="52903-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="52903-200">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="52903-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-201">Sivusto</span><span class="sxs-lookup"><span data-stu-id="52903-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-202">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="52903-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-203">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-204">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="52903-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-205">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-206">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="52903-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-207">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="52903-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-208">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="52903-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-209">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="52903-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="52903-210">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="52903-211">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="52903-212">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="52903-213">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="52903-214">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="52903-215">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="52903-216">1000</span><span class="sxs-lookup"><span data-stu-id="52903-216">1000</span></span></td>
    <td><span data-ttu-id="52903-217">1</span><span class="sxs-lookup"><span data-stu-id="52903-217">1</span></span></td>
    <td><span data-ttu-id="52903-218">14</span><span class="sxs-lookup"><span data-stu-id="52903-218">14</span></span></td>
    <td><span data-ttu-id="52903-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="52903-219">1,283.33</span></span></td>
    <td><span data-ttu-id="52903-220">14</span><span class="sxs-lookup"><span data-stu-id="52903-220">14</span></span></td>
    <td><span data-ttu-id="52903-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="52903-221">1,283.33</span></span></td>
    <td><span data-ttu-id="52903-222">91.67</span><span class="sxs-lookup"><span data-stu-id="52903-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-223">5.00</span><span class="sxs-lookup"><span data-stu-id="52903-223">5.00</span></span></td>
    <td><span data-ttu-id="52903-224">458.33</span><span class="sxs-lookup"><span data-stu-id="52903-224">458.33</span></span></td>
    <td><span data-ttu-id="52903-225">9.00</span><span class="sxs-lookup"><span data-stu-id="52903-225">9.00</span></span></td>
    <td><span data-ttu-id="52903-226">825.00</span><span class="sxs-lookup"><span data-stu-id="52903-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="52903-227">1000</span><span class="sxs-lookup"><span data-stu-id="52903-227">1000</span></span></td>
    <td><span data-ttu-id="52903-228">2</span><span class="sxs-lookup"><span data-stu-id="52903-228">2</span></span></td>
    <td><span data-ttu-id="52903-229">10</span><span class="sxs-lookup"><span data-stu-id="52903-229">10</span></span></td>
    <td><span data-ttu-id="52903-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-230">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-231">10</span><span class="sxs-lookup"><span data-stu-id="52903-231">10</span></span></td>
    <td><span data-ttu-id="52903-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-232">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-233">200.00</span><span class="sxs-lookup"><span data-stu-id="52903-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-234">10.00</span><span class="sxs-lookup"><span data-stu-id="52903-234">10.00</span></span></td>
    <td><span data-ttu-id="52903-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="52903-236"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="52903-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="52903-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="52903-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="52903-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="52903-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="52903-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="52903-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="52903-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="52903-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="52903-243">Huomaa seuraavat tiedot tässä esimerkkiraportissa:</span><span class="sxs-lookup"><span data-stu-id="52903-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="52903-244">Raportissa näkyvät **Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat taloushallinnan varastodimension arvoja (tässä tapauksessa **Toimipaikka**).</span><span class="sxs-lookup"><span data-stu-id="52903-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="52903-245">Raportti näyttää esimerkiksi toimipaikan 1 osalta seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="52903-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="52903-246">**Varaston arvon määrä** -arvo on *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="52903-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="52903-247">**Varastoarvo** -arvo on *1 283,33* (= 1,000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="52903-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="52903-248">**Keskimääräinen yksikkökustannus** -arvo on *91,67*.</span><span class="sxs-lookup"><span data-stu-id="52903-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="52903-249">Kunkin aikavälin **Varastosaldo**- ja **Summa**-arvo lasketaan käyttämällä **Keskimääräinen yksikkökustannus** -arvoa.</span><span class="sxs-lookup"><span data-stu-id="52903-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="52903-250">Raportti määrittää kunkin aikavälin varastosaldon summaamalla kunkin aikavälin vastaanotetun varastomäärän.</span><span class="sxs-lookup"><span data-stu-id="52903-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="52903-251">Se käyttää sitten FIFO-periaatetta vähentämään varasto-ottojen kokonaismäärän riippumatta siitä, mitä varastomallia nimikkeet käyttävät.</span><span class="sxs-lookup"><span data-stu-id="52903-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="52903-252">Jos suoritat saman raportin uudelleen, mutta **Toimipaikka**- ja **Varasto**-kenttien asetukseksi määritetään *Näkymä*, uusi raportti muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="52903-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="52903-253">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="52903-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-254">Sivusto</span><span class="sxs-lookup"><span data-stu-id="52903-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-255">Varasto</span><span class="sxs-lookup"><span data-stu-id="52903-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-256">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="52903-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-257">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-258">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="52903-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-259">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-260">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="52903-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-261">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="52903-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-262">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="52903-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-263">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="52903-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="52903-264">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="52903-265">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="52903-266">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="52903-267">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="52903-268">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="52903-269">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="52903-270">1000</span><span class="sxs-lookup"><span data-stu-id="52903-270">1000</span></span></td>
    <td><span data-ttu-id="52903-271">1</span><span class="sxs-lookup"><span data-stu-id="52903-271">1</span></span></td>
    <td><span data-ttu-id="52903-272">11</span><span class="sxs-lookup"><span data-stu-id="52903-272">11</span></span></td>
    <td><span data-ttu-id="52903-273">10</span><span class="sxs-lookup"><span data-stu-id="52903-273">10</span></span></td>
    <td><span data-ttu-id="52903-274">916.67</span><span class="sxs-lookup"><span data-stu-id="52903-274">916.67</span></span></td>
    <td><span data-ttu-id="52903-275">14</span><span class="sxs-lookup"><span data-stu-id="52903-275">14</span></span></td>
    <td><span data-ttu-id="52903-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="52903-276">1,283.33</span></span></td>
    <td><span data-ttu-id="52903-277">91.67</span><span class="sxs-lookup"><span data-stu-id="52903-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-278">5.00</span><span class="sxs-lookup"><span data-stu-id="52903-278">5.00</span></span></td>
    <td><span data-ttu-id="52903-279">458.33</span><span class="sxs-lookup"><span data-stu-id="52903-279">458.33</span></span></td>
    <td><span data-ttu-id="52903-280">5.00</span><span class="sxs-lookup"><span data-stu-id="52903-280">5.00</span></span></td>
    <td><span data-ttu-id="52903-281">458.33</span><span class="sxs-lookup"><span data-stu-id="52903-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="52903-282">1000</span><span class="sxs-lookup"><span data-stu-id="52903-282">1000</span></span></td>
    <td><span data-ttu-id="52903-283">1</span><span class="sxs-lookup"><span data-stu-id="52903-283">1</span></span></td>
    <td><span data-ttu-id="52903-284">12</span><span class="sxs-lookup"><span data-stu-id="52903-284">12</span></span></td>
    <td><span data-ttu-id="52903-285">4</span><span class="sxs-lookup"><span data-stu-id="52903-285">4</span></span></td>
    <td><span data-ttu-id="52903-286">366.67</span><span class="sxs-lookup"><span data-stu-id="52903-286">366.67</span></span></td>
    <td><span data-ttu-id="52903-287">14</span><span class="sxs-lookup"><span data-stu-id="52903-287">14</span></span></td>
    <td><span data-ttu-id="52903-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="52903-288">1,283.33</span></span></td>
    <td><span data-ttu-id="52903-289">91.67</span><span class="sxs-lookup"><span data-stu-id="52903-289">91.67</span></span></td>
    <td><span data-ttu-id="52903-290">4.00</span><span class="sxs-lookup"><span data-stu-id="52903-290">4.00</span></span></td>
    <td><span data-ttu-id="52903-291">366.67</span><span class="sxs-lookup"><span data-stu-id="52903-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="52903-292">1000</span><span class="sxs-lookup"><span data-stu-id="52903-292">1000</span></span></td>
    <td><span data-ttu-id="52903-293">2</span><span class="sxs-lookup"><span data-stu-id="52903-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="52903-294">10</span><span class="sxs-lookup"><span data-stu-id="52903-294">10</span></span></td>
    <td><span data-ttu-id="52903-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-295">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-296">10</span><span class="sxs-lookup"><span data-stu-id="52903-296">10</span></span></td>
    <td><span data-ttu-id="52903-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-297">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-298">200.00</span><span class="sxs-lookup"><span data-stu-id="52903-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-299">10.00</span><span class="sxs-lookup"><span data-stu-id="52903-299">10.00</span></span></td>
    <td><span data-ttu-id="52903-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="52903-301"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="52903-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="52903-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="52903-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="52903-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="52903-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="52903-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="52903-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="52903-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="52903-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="52903-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="52903-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="52903-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="52903-310">Tällä kertaa toimipaikka 1 jaetaan kahteen riviin, joista toinen on varasto 11 ja toinen varasto 12.</span><span class="sxs-lookup"><span data-stu-id="52903-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="52903-311">**Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat kuitenkin samat, koska **Varasto** ei ole taloushallinnan varastodimensio.</span><span class="sxs-lookup"><span data-stu-id="52903-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="52903-312">Huomaa myös, että toimipaikan 1 määräjakauma on erilainen.</span><span class="sxs-lookup"><span data-stu-id="52903-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="52903-313">Ensimmäisessä suoritetussa raportissa järjestelmä ohitti samassa toimipaikassa tapahtuneen siirtotilauksen ja vähensi myyntilaskun määrän toimipaikan 1 aikavälistä **31.3.2020–1.3.2020**.</span><span class="sxs-lookup"><span data-stu-id="52903-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="52903-314">Uudessa raportissa järjestelmä kuitenkin vähentää myyntilaskun määrän aikaväliltä **8.5.2020–1.5.2020** varastossa 12.</span><span class="sxs-lookup"><span data-stu-id="52903-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="52903-315">Varaston sulkemisen vaikutukset</span><span class="sxs-lookup"><span data-stu-id="52903-315">Effects of inventory closing</span></span>

<span data-ttu-id="52903-316">Jos suoritetaan varaston toukokuun sulkeminen ja sen jälkeen edellinen raportti suoritetaan uudelleen siten, että **Alkupäivämäärä**-kentän arvona on *31.5.2020*, tulokset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="52903-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="52903-317">**Varastoarvo**- ja **Keskimääräinen yksikkökustannus**-arvot on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="52903-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="52903-318">**Varastosaldo**-arvo ja kunkin aikavälin kaikki **Summa**-arvot päivitetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="52903-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="52903-319">Uusi raportti muistuttaa seuraavaa esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="52903-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="52903-320">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="52903-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-321">Sivusto</span><span class="sxs-lookup"><span data-stu-id="52903-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-322">Varasto</span><span class="sxs-lookup"><span data-stu-id="52903-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-323">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="52903-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-324">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-325">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="52903-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-326">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="52903-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="52903-327">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="52903-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-328">31.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="52903-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-329">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="52903-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="52903-330">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="52903-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="52903-331">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="52903-332">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="52903-333">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="52903-334">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="52903-335">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="52903-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="52903-336">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="52903-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="52903-337">1000</span><span class="sxs-lookup"><span data-stu-id="52903-337">1000</span></span></td>
    <td><span data-ttu-id="52903-338">1</span><span class="sxs-lookup"><span data-stu-id="52903-338">1</span></span></td>
    <td><span data-ttu-id="52903-339">11</span><span class="sxs-lookup"><span data-stu-id="52903-339">11</span></span></td>
    <td><span data-ttu-id="52903-340">10</span><span class="sxs-lookup"><span data-stu-id="52903-340">10</span></span></td>
    <td><span data-ttu-id="52903-341">910.70</span><span class="sxs-lookup"><span data-stu-id="52903-341">910.70</span></span></td>
    <td><span data-ttu-id="52903-342">14</span><span class="sxs-lookup"><span data-stu-id="52903-342">14</span></span></td>
    <td><span data-ttu-id="52903-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="52903-343">1,275.00</span></span></td>
    <td><span data-ttu-id="52903-344">91.07</span><span class="sxs-lookup"><span data-stu-id="52903-344">91.07</span></span></td>
    <td><span data-ttu-id="52903-345">0,00</span><span class="sxs-lookup"><span data-stu-id="52903-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="52903-346">5.00</span><span class="sxs-lookup"><span data-stu-id="52903-346">5.00</span></span></td>
    <td><span data-ttu-id="52903-347">455.36</span><span class="sxs-lookup"><span data-stu-id="52903-347">455.36</span></span></td>
    <td><span data-ttu-id="52903-348">5.00</span><span class="sxs-lookup"><span data-stu-id="52903-348">5.00</span></span></td>
    <td><span data-ttu-id="52903-349">455.36</span><span class="sxs-lookup"><span data-stu-id="52903-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="52903-350">1000</span><span class="sxs-lookup"><span data-stu-id="52903-350">1000</span></span></td>
    <td><span data-ttu-id="52903-351">1</span><span class="sxs-lookup"><span data-stu-id="52903-351">1</span></span></td>
    <td><span data-ttu-id="52903-352">12</span><span class="sxs-lookup"><span data-stu-id="52903-352">12</span></span></td>
    <td><span data-ttu-id="52903-353">4</span><span class="sxs-lookup"><span data-stu-id="52903-353">4</span></span></td>
    <td><span data-ttu-id="52903-354">364.29</span><span class="sxs-lookup"><span data-stu-id="52903-354">364.29</span></span></td>
    <td><span data-ttu-id="52903-355">14</span><span class="sxs-lookup"><span data-stu-id="52903-355">14</span></span></td>
    <td><span data-ttu-id="52903-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="52903-356">1,275.00</span></span></td>
    <td><span data-ttu-id="52903-357">91.07</span><span class="sxs-lookup"><span data-stu-id="52903-357">91.07</span></span></td>
    <td><span data-ttu-id="52903-358">4.00</span><span class="sxs-lookup"><span data-stu-id="52903-358">4.00</span></span></td>
    <td><span data-ttu-id="52903-359">364.29</span><span class="sxs-lookup"><span data-stu-id="52903-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="52903-360">1000</span><span class="sxs-lookup"><span data-stu-id="52903-360">1000</span></span></td>
    <td><span data-ttu-id="52903-361">2</span><span class="sxs-lookup"><span data-stu-id="52903-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="52903-362">10</span><span class="sxs-lookup"><span data-stu-id="52903-362">10</span></span></td>
    <td><span data-ttu-id="52903-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-363">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-364">10</span><span class="sxs-lookup"><span data-stu-id="52903-364">10</span></span></td>
    <td><span data-ttu-id="52903-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-365">2,000.00</span></span></td>
    <td><span data-ttu-id="52903-366">200.00</span><span class="sxs-lookup"><span data-stu-id="52903-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-367">10.00</span><span class="sxs-lookup"><span data-stu-id="52903-367">10.00</span></span></td>
    <td><span data-ttu-id="52903-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="52903-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="52903-369"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="52903-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="52903-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="52903-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="52903-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="52903-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="52903-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="52903-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="52903-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="52903-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="52903-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="52903-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="52903-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="52903-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
