---
title: Varaston erääntymisraporttien esimerkkejä ja logiikka
description: Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan varaston erääntymisraportin tuloksia.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484527"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="f7dd5-103">Varaston erääntymisraporttien esimerkkejä ja logiikka</span><span class="sxs-lookup"><span data-stu-id="f7dd5-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7dd5-104">Tässä ohjeaiheessa on esimerkkejä, jotka auttavat tulkitsemaan **Varaston erääntyminen** -raportin tuloksia.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="f7dd5-105">Tämä raportti luokittelee valitun nimikkeen tai nimikeryhmän varastosaldon ja varastoarvot useisiin aikaväleihin.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="f7dd5-106">Ohjeaiheessa myös näytetään raportin sisäinen logiikka.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="f7dd5-107">Ohjeaiheen esimerkeissä näytetään tulokset, jotka esitetään **Varaston erääntyminen** -vakioraportissa.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="f7dd5-108">Yleensä kannattaa kuitenkin käyttää tämän raportin [Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md) -versiota, etenkin jos käsiteltäviä nimikkeitä ja varastoja on paljon.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="f7dd5-109">Varaston erääntymisraportin tallennus tallentaa jokaisen luodun raportin, näyttää tulokset vuorovaikutteisena sivuna ja kaaviona sekä sallii minkä tahansa tallennetun raportin viennin.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="f7dd5-110">Esimerkeissä käytettävät mallitiedot</span><span class="sxs-lookup"><span data-stu-id="f7dd5-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="f7dd5-111">Ohjeaiheen esimerkit perustuvat tässä osassa käsiteltäviin varastotapahtuman mallitietoihin.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="f7dd5-112">Varastodimensioryhmän määritys</span><span class="sxs-lookup"><span data-stu-id="f7dd5-112">Storage dimension setup</span></span>

<span data-ttu-id="f7dd5-113">Esimerkkijärjestelmässä on seuraavat varastodimensiot.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="f7dd5-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="f7dd5-114">Name</span></span>      | <span data-ttu-id="f7dd5-115">Aktiiviset</span><span class="sxs-lookup"><span data-stu-id="f7dd5-115">Active</span></span> | <span data-ttu-id="f7dd5-116">Fyysinen varasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-116">Physical inventory</span></span> | <span data-ttu-id="f7dd5-117">Kirjanpitovarasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="f7dd5-118">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-118">Site</span></span>      | <span data-ttu-id="f7dd5-119">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-119">Yes</span></span>    | <span data-ttu-id="f7dd5-120">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-120">Yes</span></span>                | <span data-ttu-id="f7dd5-121">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-121">Yes</span></span>                 |
| <span data-ttu-id="f7dd5-122">Varasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-122">Warehouse</span></span> | <span data-ttu-id="f7dd5-123">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-123">Yes</span></span>    | <span data-ttu-id="f7dd5-124">Kyllä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-124">Yes</span></span>                | <span data-ttu-id="f7dd5-125">Nro</span><span class="sxs-lookup"><span data-stu-id="f7dd5-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="f7dd5-126">Varastomalli</span><span class="sxs-lookup"><span data-stu-id="f7dd5-126">Inventory model</span></span>

<span data-ttu-id="f7dd5-127">Esimerkkijärjestelmän vapautettujen tuotteiden varastomallin on *FIFO* ja varastomallin **Kustannushinta**-asetus on *Sisällytä fyysinen arvo*.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="f7dd5-128">Varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="f7dd5-128">Inventory transactions</span></span>

<span data-ttu-id="f7dd5-129">Esimerkkijärjestelmä sisältää seuraavat vapautetun tuotteen varastotapahtumat, kun tuotteen nimikenumero on *1000*.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="f7dd5-130">Viite</span><span class="sxs-lookup"><span data-stu-id="f7dd5-130">Reference</span></span>      | <span data-ttu-id="f7dd5-131">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-131">Site</span></span> | <span data-ttu-id="f7dd5-132">Varasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-132">Warehouse</span></span> | <span data-ttu-id="f7dd5-133">Kuitti</span><span class="sxs-lookup"><span data-stu-id="f7dd5-133">Receipt</span></span>   | <span data-ttu-id="f7dd5-134">Otto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-134">Issue</span></span> | <span data-ttu-id="f7dd5-135">Fyysinen pvm.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-135">Physical date</span></span> | <span data-ttu-id="f7dd5-136">Rahoituspvm.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-136">Financial date</span></span> | <span data-ttu-id="f7dd5-137">Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-137">Quantity</span></span> | <span data-ttu-id="f7dd5-138">Kustannussumma</span><span class="sxs-lookup"><span data-stu-id="f7dd5-138">Cost amount</span></span> | <span data-ttu-id="f7dd5-139">Fyysinen kustannus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="f7dd5-140">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-140">Purchase order</span></span> | <span data-ttu-id="f7dd5-141">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-141">1</span></span>    | <span data-ttu-id="f7dd5-142">11</span><span class="sxs-lookup"><span data-stu-id="f7dd5-142">11</span></span>        | <span data-ttu-id="f7dd5-143">Ostettu</span><span class="sxs-lookup"><span data-stu-id="f7dd5-143">Purchased</span></span> |       | <span data-ttu-id="f7dd5-144">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-144">March 15</span></span>      | <span data-ttu-id="f7dd5-145">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-145">March 15</span></span>       | <span data-ttu-id="f7dd5-146">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-146">10</span></span>       | <span data-ttu-id="f7dd5-147">1 000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-147">1,000</span></span>       | <span data-ttu-id="f7dd5-148">1 000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-148">1,000</span></span>                |
| <span data-ttu-id="f7dd5-149">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-149">Purchase order</span></span> | <span data-ttu-id="f7dd5-150">2</span><span class="sxs-lookup"><span data-stu-id="f7dd5-150">2</span></span>    | <span data-ttu-id="f7dd5-151">21</span><span class="sxs-lookup"><span data-stu-id="f7dd5-151">21</span></span>        | <span data-ttu-id="f7dd5-152">Ostettu</span><span class="sxs-lookup"><span data-stu-id="f7dd5-152">Purchased</span></span> |       | <span data-ttu-id="f7dd5-153">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-153">March 15</span></span>      | <span data-ttu-id="f7dd5-154">Maaliskuun 15.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-154">March 15</span></span>       | <span data-ttu-id="f7dd5-155">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-155">10</span></span>       | <span data-ttu-id="f7dd5-156">2,000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-156">2,000</span></span>       | <span data-ttu-id="f7dd5-157">2,000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-157">2,000</span></span>                |
| <span data-ttu-id="f7dd5-158">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-158">Purchase order</span></span> | <span data-ttu-id="f7dd5-159">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-159">1</span></span>    | <span data-ttu-id="f7dd5-160">11</span><span class="sxs-lookup"><span data-stu-id="f7dd5-160">11</span></span>        | <span data-ttu-id="f7dd5-161">Vastaanotettu</span><span class="sxs-lookup"><span data-stu-id="f7dd5-161">Received</span></span>  |       | <span data-ttu-id="f7dd5-162">Huhtikuun 15.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-162">April 15</span></span>      |                | <span data-ttu-id="f7dd5-163">5</span><span class="sxs-lookup"><span data-stu-id="f7dd5-163">5</span></span>        |             | <span data-ttu-id="f7dd5-164">375</span><span class="sxs-lookup"><span data-stu-id="f7dd5-164">375</span></span>                  |
| <span data-ttu-id="f7dd5-165">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-165">Transfer order</span></span> | <span data-ttu-id="f7dd5-166">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-166">1</span></span>    | <span data-ttu-id="f7dd5-167">11</span><span class="sxs-lookup"><span data-stu-id="f7dd5-167">11</span></span>        |           | <span data-ttu-id="f7dd5-168">Myyty</span><span class="sxs-lookup"><span data-stu-id="f7dd5-168">Sold</span></span>  | <span data-ttu-id="f7dd5-169">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-169">May 2</span></span>         | <span data-ttu-id="f7dd5-170">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-170">May 2</span></span>          | <span data-ttu-id="f7dd5-171">-5</span><span class="sxs-lookup"><span data-stu-id="f7dd5-171">-5</span></span>       | <span data-ttu-id="f7dd5-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-172">-458.33</span></span>     | <span data-ttu-id="f7dd5-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-173">-458.33</span></span>              |
| <span data-ttu-id="f7dd5-174">Siirtotilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-174">Transfer order</span></span> | <span data-ttu-id="f7dd5-175">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-175">1</span></span>    | <span data-ttu-id="f7dd5-176">12</span><span class="sxs-lookup"><span data-stu-id="f7dd5-176">12</span></span>        | <span data-ttu-id="f7dd5-177">Ostettu</span><span class="sxs-lookup"><span data-stu-id="f7dd5-177">Purchased</span></span> |       | <span data-ttu-id="f7dd5-178">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-178">May 2</span></span>         | <span data-ttu-id="f7dd5-179">Toukokuun 2.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-179">May 2</span></span>          | <span data-ttu-id="f7dd5-180">5</span><span class="sxs-lookup"><span data-stu-id="f7dd5-180">5</span></span>        | <span data-ttu-id="f7dd5-181">458.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-181">458.33</span></span>      | <span data-ttu-id="f7dd5-182">458.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-182">458.33</span></span>               |
| <span data-ttu-id="f7dd5-183">Myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-183">Sales order</span></span>    | <span data-ttu-id="f7dd5-184">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-184">1</span></span>    | <span data-ttu-id="f7dd5-185">12</span><span class="sxs-lookup"><span data-stu-id="f7dd5-185">12</span></span>        |           | <span data-ttu-id="f7dd5-186">Myyty</span><span class="sxs-lookup"><span data-stu-id="f7dd5-186">Sold</span></span>  | <span data-ttu-id="f7dd5-187">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-187">May 3</span></span>         | <span data-ttu-id="f7dd5-188">Toukokuun 3.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-188">May 3</span></span>          | <span data-ttu-id="f7dd5-189">-1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-189">-1</span></span>       | <span data-ttu-id="f7dd5-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-190">-91.67</span></span>      | <span data-ttu-id="f7dd5-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="f7dd5-192">Kunkin aikavälin määrien ja summien laskeminen</span><span class="sxs-lookup"><span data-stu-id="f7dd5-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="f7dd5-193">Edellisissä osissa kuvattuja mallitietoja käyttämällä voit suorittaa **Varaston erääntyminen** -raportin, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="f7dd5-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="f7dd5-194">**Alkupäivämäärä:** *9.5.2020*</span><span class="sxs-lookup"><span data-stu-id="f7dd5-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="f7dd5-195">**Paikka:** *Näkymä*</span><span class="sxs-lookup"><span data-stu-id="f7dd5-195">**Site:** *View*</span></span>
- <span data-ttu-id="f7dd5-196">**Varasto**: *Ei*</span><span class="sxs-lookup"><span data-stu-id="f7dd5-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="f7dd5-197">**Nimiketunnus:** *Yhteensä*</span><span class="sxs-lookup"><span data-stu-id="f7dd5-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="f7dd5-198">**Erääntymiskausi:** Tämän kentän käyttäminen luo kuukausittaiset aikavälit.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="f7dd5-199">Tässä tapauksessa luotu luodun raportin sisältö muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="f7dd5-200">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-201">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-202">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-203">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-204">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-205">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-206">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-207">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-208">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-209">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="f7dd5-210">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-211">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-212">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-213">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-214">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-215">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="f7dd5-216">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-216">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-217">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-217">1</span></span></td>
    <td><span data-ttu-id="f7dd5-218">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-218">14</span></span></td>
    <td><span data-ttu-id="f7dd5-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-219">1,283.33</span></span></td>
    <td><span data-ttu-id="f7dd5-220">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-220">14</span></span></td>
    <td><span data-ttu-id="f7dd5-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-221">1,283.33</span></span></td>
    <td><span data-ttu-id="f7dd5-222">91.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-223">5.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-223">5.00</span></span></td>
    <td><span data-ttu-id="f7dd5-224">458.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-224">458.33</span></span></td>
    <td><span data-ttu-id="f7dd5-225">9.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-225">9.00</span></span></td>
    <td><span data-ttu-id="f7dd5-226">825.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="f7dd5-227">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-227">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-228">2</span><span class="sxs-lookup"><span data-stu-id="f7dd5-228">2</span></span></td>
    <td><span data-ttu-id="f7dd5-229">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-229">10</span></span></td>
    <td><span data-ttu-id="f7dd5-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-230">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-231">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-231">10</span></span></td>
    <td><span data-ttu-id="f7dd5-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-232">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-233">200.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-234">10.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-234">10.00</span></span></td>
    <td><span data-ttu-id="f7dd5-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="f7dd5-236"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="f7dd5-243">Huomaa seuraavat tiedot tässä esimerkkiraportissa:</span><span class="sxs-lookup"><span data-stu-id="f7dd5-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="f7dd5-244">Raportissa näkyvät **Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat taloushallinnan varastodimension arvoja (tässä tapauksessa **Toimipaikka**).</span><span class="sxs-lookup"><span data-stu-id="f7dd5-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="f7dd5-245">Raportti näyttää esimerkiksi toimipaikan 1 osalta seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="f7dd5-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="f7dd5-246">**Varaston arvon määrä** -arvo on *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="f7dd5-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="f7dd5-247">**Varastoarvo** -arvo on *1 283,33* (= 1,000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="f7dd5-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="f7dd5-248">**Keskimääräinen yksikkökustannus** -arvo on *91,67*.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="f7dd5-249">Kunkin aikavälin **Varastosaldo**- ja **Summa**-arvo lasketaan käyttämällä **Keskimääräinen yksikkökustannus** -arvoa.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="f7dd5-250">Raportti määrittää kunkin aikavälin varastosaldon summaamalla kunkin aikavälin vastaanotetun varastomäärän.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="f7dd5-251">Se käyttää sitten FIFO-periaatetta vähentämään varasto-ottojen kokonaismäärän riippumatta siitä, mitä varastomallia nimikkeet käyttävät.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="f7dd5-252">Jos suoritat saman raportin uudelleen, mutta **Toimipaikka**- ja **Varasto**-kenttien asetukseksi määritetään *Näkymä*, uusi raportti muistuttaa seuraavaa esimerkkiä.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="f7dd5-253">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-254">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-255">Varasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-256">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-257">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-258">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-259">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-260">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-261">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-262">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-263">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="f7dd5-264">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-265">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-266">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-267">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-268">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-269">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="f7dd5-270">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-270">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-271">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-271">1</span></span></td>
    <td><span data-ttu-id="f7dd5-272">11</span><span class="sxs-lookup"><span data-stu-id="f7dd5-272">11</span></span></td>
    <td><span data-ttu-id="f7dd5-273">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-273">10</span></span></td>
    <td><span data-ttu-id="f7dd5-274">916.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-274">916.67</span></span></td>
    <td><span data-ttu-id="f7dd5-275">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-275">14</span></span></td>
    <td><span data-ttu-id="f7dd5-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-276">1,283.33</span></span></td>
    <td><span data-ttu-id="f7dd5-277">91.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-278">5.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-278">5.00</span></span></td>
    <td><span data-ttu-id="f7dd5-279">458.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-279">458.33</span></span></td>
    <td><span data-ttu-id="f7dd5-280">5.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-280">5.00</span></span></td>
    <td><span data-ttu-id="f7dd5-281">458.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="f7dd5-282">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-282">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-283">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-283">1</span></span></td>
    <td><span data-ttu-id="f7dd5-284">12</span><span class="sxs-lookup"><span data-stu-id="f7dd5-284">12</span></span></td>
    <td><span data-ttu-id="f7dd5-285">4</span><span class="sxs-lookup"><span data-stu-id="f7dd5-285">4</span></span></td>
    <td><span data-ttu-id="f7dd5-286">366.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-286">366.67</span></span></td>
    <td><span data-ttu-id="f7dd5-287">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-287">14</span></span></td>
    <td><span data-ttu-id="f7dd5-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="f7dd5-288">1,283.33</span></span></td>
    <td><span data-ttu-id="f7dd5-289">91.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-289">91.67</span></span></td>
    <td><span data-ttu-id="f7dd5-290">4.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-290">4.00</span></span></td>
    <td><span data-ttu-id="f7dd5-291">366.67</span><span class="sxs-lookup"><span data-stu-id="f7dd5-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="f7dd5-292">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-292">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-293">2</span><span class="sxs-lookup"><span data-stu-id="f7dd5-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-294">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-294">10</span></span></td>
    <td><span data-ttu-id="f7dd5-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-295">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-296">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-296">10</span></span></td>
    <td><span data-ttu-id="f7dd5-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-297">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-298">200.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-299">10.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-299">10.00</span></span></td>
    <td><span data-ttu-id="f7dd5-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="f7dd5-301"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="f7dd5-310">Tällä kertaa toimipaikka 1 jaetaan kahteen riviin, joista toinen on varasto 11 ja toinen varasto 12.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="f7dd5-311">**Varaston arvon määrä**-, **Varastoarvo**- ja **Keskimääräinen yksikkökustannus** -arvot ovat kuitenkin samat, koska **Varasto** ei ole taloushallinnan varastodimensio.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="f7dd5-312">Huomaa myös, että toimipaikan 1 määräjakauma on erilainen.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="f7dd5-313">Ensimmäisessä suoritetussa raportissa järjestelmä ohitti samassa toimipaikassa tapahtuneen siirtotilauksen ja vähensi myyntilaskun määrän toimipaikan 1 aikavälistä **31.3.2020–1.3.2020**.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="f7dd5-314">Uudessa raportissa järjestelmä kuitenkin vähentää myyntilaskun määrän aikaväliltä **8.5.2020–1.5.2020** varastossa 12.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="f7dd5-315">Varaston sulkemisen vaikutukset</span><span class="sxs-lookup"><span data-stu-id="f7dd5-315">Effects of inventory closing</span></span>

<span data-ttu-id="f7dd5-316">Jos suoritetaan varaston toukokuun sulkeminen ja sen jälkeen edellinen raportti suoritetaan uudelleen siten, että **Alkupäivämäärä**-kentän arvona on *31.5.2020*, tulokset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="f7dd5-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="f7dd5-317">**Varastoarvo**- ja **Keskimääräinen yksikkökustannus**-arvot on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="f7dd5-318">**Varastosaldo**-arvo ja kunkin aikavälin kaikki **Summa**-arvot päivitetään vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="f7dd5-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="f7dd5-319">Uusi raportti muistuttaa seuraavaa esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="f7dd5-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="f7dd5-320">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-321">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-322">Varasto</span><span class="sxs-lookup"><span data-stu-id="f7dd5-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-323">Varastosaldo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-324">Käytettävissä olevan varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-325">Varaston arvon määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-326">Varaston arvo</span><span class="sxs-lookup"><span data-stu-id="f7dd5-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="f7dd5-327">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="f7dd5-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-328">31.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-329">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="f7dd5-330">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="f7dd5-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="f7dd5-331">P1:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-332">P1:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-333">P2:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-334">P2:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="f7dd5-335">P3:Määrä</span><span class="sxs-lookup"><span data-stu-id="f7dd5-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="f7dd5-336">P3:Summa</span><span class="sxs-lookup"><span data-stu-id="f7dd5-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="f7dd5-337">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-337">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-338">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-338">1</span></span></td>
    <td><span data-ttu-id="f7dd5-339">11</span><span class="sxs-lookup"><span data-stu-id="f7dd5-339">11</span></span></td>
    <td><span data-ttu-id="f7dd5-340">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-340">10</span></span></td>
    <td><span data-ttu-id="f7dd5-341">910.70</span><span class="sxs-lookup"><span data-stu-id="f7dd5-341">910.70</span></span></td>
    <td><span data-ttu-id="f7dd5-342">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-342">14</span></span></td>
    <td><span data-ttu-id="f7dd5-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-343">1,275.00</span></span></td>
    <td><span data-ttu-id="f7dd5-344">91.07</span><span class="sxs-lookup"><span data-stu-id="f7dd5-344">91.07</span></span></td>
    <td><span data-ttu-id="f7dd5-345">0,00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-346">5.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-346">5.00</span></span></td>
    <td><span data-ttu-id="f7dd5-347">455.36</span><span class="sxs-lookup"><span data-stu-id="f7dd5-347">455.36</span></span></td>
    <td><span data-ttu-id="f7dd5-348">5.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-348">5.00</span></span></td>
    <td><span data-ttu-id="f7dd5-349">455.36</span><span class="sxs-lookup"><span data-stu-id="f7dd5-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="f7dd5-350">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-350">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-351">1</span><span class="sxs-lookup"><span data-stu-id="f7dd5-351">1</span></span></td>
    <td><span data-ttu-id="f7dd5-352">12</span><span class="sxs-lookup"><span data-stu-id="f7dd5-352">12</span></span></td>
    <td><span data-ttu-id="f7dd5-353">4</span><span class="sxs-lookup"><span data-stu-id="f7dd5-353">4</span></span></td>
    <td><span data-ttu-id="f7dd5-354">364.29</span><span class="sxs-lookup"><span data-stu-id="f7dd5-354">364.29</span></span></td>
    <td><span data-ttu-id="f7dd5-355">14</span><span class="sxs-lookup"><span data-stu-id="f7dd5-355">14</span></span></td>
    <td><span data-ttu-id="f7dd5-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-356">1,275.00</span></span></td>
    <td><span data-ttu-id="f7dd5-357">91.07</span><span class="sxs-lookup"><span data-stu-id="f7dd5-357">91.07</span></span></td>
    <td><span data-ttu-id="f7dd5-358">4.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-358">4.00</span></span></td>
    <td><span data-ttu-id="f7dd5-359">364.29</span><span class="sxs-lookup"><span data-stu-id="f7dd5-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="f7dd5-360">1000</span><span class="sxs-lookup"><span data-stu-id="f7dd5-360">1000</span></span></td>
    <td><span data-ttu-id="f7dd5-361">2</span><span class="sxs-lookup"><span data-stu-id="f7dd5-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-362">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-362">10</span></span></td>
    <td><span data-ttu-id="f7dd5-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-363">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-364">10</span><span class="sxs-lookup"><span data-stu-id="f7dd5-364">10</span></span></td>
    <td><span data-ttu-id="f7dd5-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-365">2,000.00</span></span></td>
    <td><span data-ttu-id="f7dd5-366">200.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-367">10.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-367">10.00</span></span></td>
    <td><span data-ttu-id="f7dd5-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="f7dd5-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="f7dd5-369"><strong>1 000 Summat</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="f7dd5-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="f7dd5-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="f7dd5-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
