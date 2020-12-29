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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427054"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="e3ca3-103">Varaston erääntymisraporttien esimerkkejä ja logiikka</span><span class="sxs-lookup"><span data-stu-id="e3ca3-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3ca3-104">Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan **Varaston erääntyminen** -raportin tuloksia.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="e3ca3-105">Tämä raportti luokittelee valitun nimikkeen tai nimikeryhmän varastosaldon ja varastoarvot useisiin aikaväleihin.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="e3ca3-106">Ohjeaiheessa myös näytetään raportin sisäinen logiikka.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="e3ca3-107">Ohjeaiheen esimerkeissä näytetään tulokset, jotka esitetään **Varaston erääntyminen** -vakioraportissa.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="e3ca3-108">Yleensä kannattaa kuitenkin käyttää tämän raportin [Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md) -versiota, etenkin jos käsiteltäviä nimikkeitä ja varastoja on paljon.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="e3ca3-109">Varaston erääntymisraportin tallennus tallentaa jokaisen luodun raportin, näyttää tulokset vuorovaikutteisena sivuna ja kaaviona sekä sallii minkä tahansa tallennetun raportin viennin.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="e3ca3-110">Esimerkeissä käytettävät mallitiedot</span><span class="sxs-lookup"><span data-stu-id="e3ca3-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="e3ca3-111">Ohjeaiheen esimerkit perustuvat tässä osassa käsiteltäviin varastotapahtuman mallitietoihin.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="e3ca3-112">Varastodimensioryhmän määritys</span><span class="sxs-lookup"><span data-stu-id="e3ca3-112">Storage dimension setup</span></span>

<span data-ttu-id="e3ca3-113">Esimerkkijärjestelmässä on seuraavat varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="e3ca3-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="e3ca3-114">Name</span></span>      | <span data-ttu-id="e3ca3-115">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="e3ca3-115">Active</span></span> | <span data-ttu-id="e3ca3-116">Fyysinen varasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-116">Physical inventory</span></span> | <span data-ttu-id="e3ca3-117">Kirjanpitovarasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="e3ca3-118">Sivusto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-118">Site</span></span>      | <span data-ttu-id="e3ca3-119">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-119">Yes</span></span>    | <span data-ttu-id="e3ca3-120">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-120">Yes</span></span>                | <span data-ttu-id="e3ca3-121">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-121">Yes</span></span>                 |
| <span data-ttu-id="e3ca3-122">Varasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-122">Warehouse</span></span> | <span data-ttu-id="e3ca3-123">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-123">Yes</span></span>    | <span data-ttu-id="e3ca3-124">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-124">Yes</span></span>                | <span data-ttu-id="e3ca3-125">Nro</span><span class="sxs-lookup"><span data-stu-id="e3ca3-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="e3ca3-126">Varastomalli</span><span class="sxs-lookup"><span data-stu-id="e3ca3-126">Inventory model</span></span>

<span data-ttu-id="e3ca3-127">Esimerkkijärjestelmän vapautettujen tuotteiden varastomallin on *FIFO* ja varastomallin **Kustannushinta**-asetus on *Sisällytä fyysinen arvo*.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="e3ca3-128">Varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="e3ca3-128">Inventory transactions</span></span>

<span data-ttu-id="e3ca3-129">Esimerkkijärjestelmä sisältää seuraavat vapautetun tuotteen varastotapahtumat, kun tuotteen nimikenumero on *1000*.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="e3ca3-130">Viite</span><span class="sxs-lookup"><span data-stu-id="e3ca3-130">Reference</span></span>      | <span data-ttu-id="e3ca3-131">Sivusto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-131">Site</span></span> | <span data-ttu-id="e3ca3-132">Varasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-132">Warehouse</span></span> | <span data-ttu-id="e3ca3-133">Kuitti</span><span class="sxs-lookup"><span data-stu-id="e3ca3-133">Receipt</span></span>   | <span data-ttu-id="e3ca3-134">Otto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-134">Issue</span></span> | <span data-ttu-id="e3ca3-135">Fyysinen pvm.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-135">Physical date</span></span> | <span data-ttu-id="e3ca3-136">Rahoituspvm.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-136">Financial date</span></span> | <span data-ttu-id="e3ca3-137">Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-137">Quantity</span></span> | <span data-ttu-id="e3ca3-138">Kustannussumma</span><span class="sxs-lookup"><span data-stu-id="e3ca3-138">Cost amount</span></span> | <span data-ttu-id="e3ca3-139">Fyysinen kustannus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="e3ca3-140">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-140">Purchase order</span></span> | <span data-ttu-id="e3ca3-141">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-141">1</span></span>    | <span data-ttu-id="e3ca3-142">11</span><span class="sxs-lookup"><span data-stu-id="e3ca3-142">11</span></span>        | <span data-ttu-id="e3ca3-143">Ostettu</span><span class="sxs-lookup"><span data-stu-id="e3ca3-143">Purchased</span></span> |       | <span data-ttu-id="e3ca3-144">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-144">March 15</span></span>      | <span data-ttu-id="e3ca3-145">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-145">March 15</span></span>       | <span data-ttu-id="e3ca3-146">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-146">10</span></span>       | <span data-ttu-id="e3ca3-147">1 000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-147">1,000</span></span>       | <span data-ttu-id="e3ca3-148">1 000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-148">1,000</span></span>                |
| <span data-ttu-id="e3ca3-149">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-149">Purchase order</span></span> | <span data-ttu-id="e3ca3-150">2</span><span class="sxs-lookup"><span data-stu-id="e3ca3-150">2</span></span>    | <span data-ttu-id="e3ca3-151">21</span><span class="sxs-lookup"><span data-stu-id="e3ca3-151">21</span></span>        | <span data-ttu-id="e3ca3-152">Ostettu</span><span class="sxs-lookup"><span data-stu-id="e3ca3-152">Purchased</span></span> |       | <span data-ttu-id="e3ca3-153">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-153">March 15</span></span>      | <span data-ttu-id="e3ca3-154">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-154">March 15</span></span>       | <span data-ttu-id="e3ca3-155">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-155">10</span></span>       | <span data-ttu-id="e3ca3-156">2,000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-156">2,000</span></span>       | <span data-ttu-id="e3ca3-157">2,000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-157">2,000</span></span>                |
| <span data-ttu-id="e3ca3-158">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-158">Purchase order</span></span> | <span data-ttu-id="e3ca3-159">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-159">1</span></span>    | <span data-ttu-id="e3ca3-160">11</span><span class="sxs-lookup"><span data-stu-id="e3ca3-160">11</span></span>        | <span data-ttu-id="e3ca3-161">Vastaanotettu</span><span class="sxs-lookup"><span data-stu-id="e3ca3-161">Received</span></span>  |       | <span data-ttu-id="e3ca3-162">Huhtikuun 15.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-162">April 15</span></span>      |                | <span data-ttu-id="e3ca3-163">5</span><span class="sxs-lookup"><span data-stu-id="e3ca3-163">5</span></span>        |             | <span data-ttu-id="e3ca3-164">375</span><span class="sxs-lookup"><span data-stu-id="e3ca3-164">375</span></span>                  |
| <span data-ttu-id="e3ca3-165">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-165">Transfer order</span></span> | <span data-ttu-id="e3ca3-166">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-166">1</span></span>    | <span data-ttu-id="e3ca3-167">11</span><span class="sxs-lookup"><span data-stu-id="e3ca3-167">11</span></span>        |           | <span data-ttu-id="e3ca3-168">Myyty</span><span class="sxs-lookup"><span data-stu-id="e3ca3-168">Sold</span></span>  | <span data-ttu-id="e3ca3-169">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-169">May 2</span></span>         | <span data-ttu-id="e3ca3-170">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-170">May 2</span></span>          | <span data-ttu-id="e3ca3-171">-5</span><span class="sxs-lookup"><span data-stu-id="e3ca3-171">-5</span></span>       | <span data-ttu-id="e3ca3-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-172">-458.33</span></span>     | <span data-ttu-id="e3ca3-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-173">-458.33</span></span>              |
| <span data-ttu-id="e3ca3-174">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-174">Transfer order</span></span> | <span data-ttu-id="e3ca3-175">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-175">1</span></span>    | <span data-ttu-id="e3ca3-176">12</span><span class="sxs-lookup"><span data-stu-id="e3ca3-176">12</span></span>        | <span data-ttu-id="e3ca3-177">Ostettu</span><span class="sxs-lookup"><span data-stu-id="e3ca3-177">Purchased</span></span> |       | <span data-ttu-id="e3ca3-178">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-178">May 2</span></span>         | <span data-ttu-id="e3ca3-179">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-179">May 2</span></span>          | <span data-ttu-id="e3ca3-180">5</span><span class="sxs-lookup"><span data-stu-id="e3ca3-180">5</span></span>        | <span data-ttu-id="e3ca3-181">458.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-181">458.33</span></span>      | <span data-ttu-id="e3ca3-182">458.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-182">458.33</span></span>               |
| <span data-ttu-id="e3ca3-183">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-183">Sales order</span></span>    | <span data-ttu-id="e3ca3-184">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-184">1</span></span>    | <span data-ttu-id="e3ca3-185">12</span><span class="sxs-lookup"><span data-stu-id="e3ca3-185">12</span></span>        |           | <span data-ttu-id="e3ca3-186">Myyty</span><span class="sxs-lookup"><span data-stu-id="e3ca3-186">Sold</span></span>  | <span data-ttu-id="e3ca3-187">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-187">May 3</span></span>         | <span data-ttu-id="e3ca3-188">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-188">May 3</span></span>          | <span data-ttu-id="e3ca3-189">-1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-189">-1</span></span>       | <span data-ttu-id="e3ca3-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-190">-91.67</span></span>      | <span data-ttu-id="e3ca3-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="e3ca3-192">Kunkin aikavälin määrien ja summien laskeminen</span><span class="sxs-lookup"><span data-stu-id="e3ca3-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="e3ca3-193">Edellisissä osissa kuvattuja mallitietoja käyttämällä voit suorittaa **Varaston erääntyminen** -raportin, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="e3ca3-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="e3ca3-194">**Alkupäivämäärä:** *9.5.2020*</span><span class="sxs-lookup"><span data-stu-id="e3ca3-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="e3ca3-195">**Paikka:** *Näkymä*</span><span class="sxs-lookup"><span data-stu-id="e3ca3-195">**Site:** *View*</span></span>
- <span data-ttu-id="e3ca3-196">**Varasto**: *Ei*</span><span class="sxs-lookup"><span data-stu-id="e3ca3-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="e3ca3-197">**Nimiketunnus:** *Yhteensä*</span><span class="sxs-lookup"><span data-stu-id="e3ca3-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="e3ca3-198">**Erääntymiskausi:** Tämän kentän käyttäminen luo kuukausittaiset aikavälit.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="e3ca3-199">Tässä tapauksessa luotu luodun raportin sisältö muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e3ca3-200">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-201">Sivusto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-202">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-203">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-204">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-205">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-206">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-207">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-208">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-209">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e3ca3-210">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-211">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-212">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-213">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-214">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-215">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e3ca3-216">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-216">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-217">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-217">1</span></span></td>
    <td><span data-ttu-id="e3ca3-218">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-218">14</span></span></td>
    <td><span data-ttu-id="e3ca3-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-219">1,283.33</span></span></td>
    <td><span data-ttu-id="e3ca3-220">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-220">14</span></span></td>
    <td><span data-ttu-id="e3ca3-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-221">1,283.33</span></span></td>
    <td><span data-ttu-id="e3ca3-222">91.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-223">5.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-223">5.00</span></span></td>
    <td><span data-ttu-id="e3ca3-224">458.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-224">458.33</span></span></td>
    <td><span data-ttu-id="e3ca3-225">9.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-225">9.00</span></span></td>
    <td><span data-ttu-id="e3ca3-226">825.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e3ca3-227">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-227">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-228">2</span><span class="sxs-lookup"><span data-stu-id="e3ca3-228">2</span></span></td>
    <td><span data-ttu-id="e3ca3-229">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-229">10</span></span></td>
    <td><span data-ttu-id="e3ca3-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-230">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-231">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-231">10</span></span></td>
    <td><span data-ttu-id="e3ca3-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-232">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-233">200.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-234">10.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-234">10.00</span></span></td>
    <td><span data-ttu-id="e3ca3-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e3ca3-236"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="e3ca3-243">Huomaa seuraavat tiedot tässä esimerkkiraportissa:</span><span class="sxs-lookup"><span data-stu-id="e3ca3-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="e3ca3-244">Raportissa näkyvät **Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat taloushallinnan varastodimension arvoja (tässä tapauksessa **Toimipaikka**).</span><span class="sxs-lookup"><span data-stu-id="e3ca3-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="e3ca3-245">Raportti näyttää esimerkiksi toimipaikan 1 osalta seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="e3ca3-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="e3ca3-246">**Varaston arvon määrä** -arvo on *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="e3ca3-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="e3ca3-247">**Varastoarvo** -arvo on *1 283,33* (= 1,000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="e3ca3-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="e3ca3-248">**Keskimääräinen yksikkökustannus** -arvo on *91,67*.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="e3ca3-249">Kunkin aikavälin **Varastosaldo**- ja **Summa**-arvo lasketaan käyttämällä **Keskimääräinen yksikkökustannus** -arvoa.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="e3ca3-250">Raportti määrittää kunkin aikavälin varastosaldon summaamalla kunkin aikavälin vastaanotetun varastomäärän.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="e3ca3-251">Se käyttää sitten FIFO-periaatetta vähentämään varasto-ottojen kokonaismäärän riippumatta siitä, mitä varastomallia nimikkeet käyttävät.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="e3ca3-252">Jos suoritat saman raportin uudelleen, mutta **Toimipaikka**- ja **Varasto**-kenttien asetukseksi määritetään *Näkymä*, uusi raportti muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e3ca3-253">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-254">Sivusto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-255">Varasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-256">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-257">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-258">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-259">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-260">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-261">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-262">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-263">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e3ca3-264">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-265">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-266">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-267">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-268">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-269">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e3ca3-270">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-270">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-271">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-271">1</span></span></td>
    <td><span data-ttu-id="e3ca3-272">11</span><span class="sxs-lookup"><span data-stu-id="e3ca3-272">11</span></span></td>
    <td><span data-ttu-id="e3ca3-273">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-273">10</span></span></td>
    <td><span data-ttu-id="e3ca3-274">916.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-274">916.67</span></span></td>
    <td><span data-ttu-id="e3ca3-275">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-275">14</span></span></td>
    <td><span data-ttu-id="e3ca3-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-276">1,283.33</span></span></td>
    <td><span data-ttu-id="e3ca3-277">91.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-278">5.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-278">5.00</span></span></td>
    <td><span data-ttu-id="e3ca3-279">458.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-279">458.33</span></span></td>
    <td><span data-ttu-id="e3ca3-280">5.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-280">5.00</span></span></td>
    <td><span data-ttu-id="e3ca3-281">458.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e3ca3-282">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-282">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-283">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-283">1</span></span></td>
    <td><span data-ttu-id="e3ca3-284">12</span><span class="sxs-lookup"><span data-stu-id="e3ca3-284">12</span></span></td>
    <td><span data-ttu-id="e3ca3-285">4</span><span class="sxs-lookup"><span data-stu-id="e3ca3-285">4</span></span></td>
    <td><span data-ttu-id="e3ca3-286">366.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-286">366.67</span></span></td>
    <td><span data-ttu-id="e3ca3-287">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-287">14</span></span></td>
    <td><span data-ttu-id="e3ca3-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="e3ca3-288">1,283.33</span></span></td>
    <td><span data-ttu-id="e3ca3-289">91.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-289">91.67</span></span></td>
    <td><span data-ttu-id="e3ca3-290">4.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-290">4.00</span></span></td>
    <td><span data-ttu-id="e3ca3-291">366.67</span><span class="sxs-lookup"><span data-stu-id="e3ca3-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="e3ca3-292">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-292">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-293">2</span><span class="sxs-lookup"><span data-stu-id="e3ca3-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-294">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-294">10</span></span></td>
    <td><span data-ttu-id="e3ca3-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-295">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-296">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-296">10</span></span></td>
    <td><span data-ttu-id="e3ca3-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-297">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-298">200.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-299">10.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-299">10.00</span></span></td>
    <td><span data-ttu-id="e3ca3-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e3ca3-301"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="e3ca3-310">Tällä kertaa toimipaikka 1 jaetaan kahteen riviin, joista toinen on varasto 11 ja toinen varasto 12.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="e3ca3-311">**Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat kuitenkin samat, koska **Varasto** ei ole taloushallinnan varastodimensio.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="e3ca3-312">Huomaa myös, että toimipaikan 1 määräjakauma on erilainen.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="e3ca3-313">Ensimmäisessä suoritetussa raportissa järjestelmä ohitti samassa toimipaikassa tapahtuneen siirtotilauksen ja vähensi myyntilaskun määrän toimipaikan 1 aikavälistä **31.3.2020–1.3.2020**.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="e3ca3-314">Uudessa raportissa järjestelmä kuitenkin vähentää myyntilaskun määrän aikaväliltä **8.5.2020–1.5.2020** varastossa 12.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="e3ca3-315">Varaston sulkemisen vaikutukset</span><span class="sxs-lookup"><span data-stu-id="e3ca3-315">Effects of inventory closing</span></span>

<span data-ttu-id="e3ca3-316">Jos suoritetaan varaston toukokuun sulkeminen ja sen jälkeen edellinen raportti suoritetaan uudelleen siten, että **Alkupäivämäärä**-kentän arvona on *31.5.2020*, tulokset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="e3ca3-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="e3ca3-317">**Varastoarvo**- ja **Keskimääräinen yksikkökustannus**-arvot on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="e3ca3-318">**Varastosaldo**-arvo ja kunkin aikavälin kaikki **Summa**-arvot päivitetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="e3ca3-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="e3ca3-319">Uusi raportti muistuttaa seuraavaa esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="e3ca3-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="e3ca3-320">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-321">Sivusto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-322">Varasto</span><span class="sxs-lookup"><span data-stu-id="e3ca3-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-323">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-324">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-325">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-326">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="e3ca3-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="e3ca3-327">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="e3ca3-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-328">31.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-329">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="e3ca3-330">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="e3ca3-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="e3ca3-331">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-332">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-333">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-334">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="e3ca3-335">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="e3ca3-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="e3ca3-336">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="e3ca3-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="e3ca3-337">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-337">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-338">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-338">1</span></span></td>
    <td><span data-ttu-id="e3ca3-339">11</span><span class="sxs-lookup"><span data-stu-id="e3ca3-339">11</span></span></td>
    <td><span data-ttu-id="e3ca3-340">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-340">10</span></span></td>
    <td><span data-ttu-id="e3ca3-341">910.70</span><span class="sxs-lookup"><span data-stu-id="e3ca3-341">910.70</span></span></td>
    <td><span data-ttu-id="e3ca3-342">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-342">14</span></span></td>
    <td><span data-ttu-id="e3ca3-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-343">1,275.00</span></span></td>
    <td><span data-ttu-id="e3ca3-344">91.07</span><span class="sxs-lookup"><span data-stu-id="e3ca3-344">91.07</span></span></td>
    <td><span data-ttu-id="e3ca3-345">0,00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-346">5.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-346">5.00</span></span></td>
    <td><span data-ttu-id="e3ca3-347">455.36</span><span class="sxs-lookup"><span data-stu-id="e3ca3-347">455.36</span></span></td>
    <td><span data-ttu-id="e3ca3-348">5.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-348">5.00</span></span></td>
    <td><span data-ttu-id="e3ca3-349">455.36</span><span class="sxs-lookup"><span data-stu-id="e3ca3-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="e3ca3-350">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-350">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-351">1</span><span class="sxs-lookup"><span data-stu-id="e3ca3-351">1</span></span></td>
    <td><span data-ttu-id="e3ca3-352">12</span><span class="sxs-lookup"><span data-stu-id="e3ca3-352">12</span></span></td>
    <td><span data-ttu-id="e3ca3-353">4</span><span class="sxs-lookup"><span data-stu-id="e3ca3-353">4</span></span></td>
    <td><span data-ttu-id="e3ca3-354">364.29</span><span class="sxs-lookup"><span data-stu-id="e3ca3-354">364.29</span></span></td>
    <td><span data-ttu-id="e3ca3-355">14</span><span class="sxs-lookup"><span data-stu-id="e3ca3-355">14</span></span></td>
    <td><span data-ttu-id="e3ca3-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-356">1,275.00</span></span></td>
    <td><span data-ttu-id="e3ca3-357">91.07</span><span class="sxs-lookup"><span data-stu-id="e3ca3-357">91.07</span></span></td>
    <td><span data-ttu-id="e3ca3-358">4.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-358">4.00</span></span></td>
    <td><span data-ttu-id="e3ca3-359">364.29</span><span class="sxs-lookup"><span data-stu-id="e3ca3-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="e3ca3-360">1000</span><span class="sxs-lookup"><span data-stu-id="e3ca3-360">1000</span></span></td>
    <td><span data-ttu-id="e3ca3-361">2</span><span class="sxs-lookup"><span data-stu-id="e3ca3-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-362">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-362">10</span></span></td>
    <td><span data-ttu-id="e3ca3-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-363">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-364">10</span><span class="sxs-lookup"><span data-stu-id="e3ca3-364">10</span></span></td>
    <td><span data-ttu-id="e3ca3-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-365">2,000.00</span></span></td>
    <td><span data-ttu-id="e3ca3-366">200.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-367">10.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-367">10.00</span></span></td>
    <td><span data-ttu-id="e3ca3-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="e3ca3-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="e3ca3-369"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="e3ca3-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="e3ca3-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="e3ca3-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
