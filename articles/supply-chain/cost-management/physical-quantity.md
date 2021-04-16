---
title: Varasto-objektin arvot
description: Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52f39c18888b94b533743f546554d5cd1b2d56df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832247"
---
# <a name="inventory-object-values"></a><span data-ttu-id="2190b-103">Varasto-objektin arvot</span><span class="sxs-lookup"><span data-stu-id="2190b-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2190b-104">Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="2190b-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="2190b-105">**Fyysinen määrä**-nimisen uuden toiminnon avulla näet tietyn varasto-objektin arvot.</span><span class="sxs-lookup"><span data-stu-id="2190b-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="2190b-106">Kustannusobjekti edustaa sen yksikön tasoa, jolla varaston kirjanpito suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="2190b-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="2190b-107">Lisätietoja kustannusobjekteista on kohdassa [Kustannusobjektit](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="2190b-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="2190b-108">Saat tietyn varasto-objektin arvot näkyviin valitsemalla **Fyysinen määrä** **Kustannusobjekti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2190b-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="2190b-109">Varasto-objektin arvo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="2190b-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="2190b-110">Varasto-objekti.Arvo = Kustannusobjekti.Keskimääräinen yksikkökustannus × Varasto-objekti.Määrä</span><span class="sxs-lookup"><span data-stu-id="2190b-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="2190b-111">Seuraavassa esimerkissä näytetään, miten varasto-objektin ja kustannusobjektin arvot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="2190b-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="2190b-112">Nimikkeelle A on rekisteröity kaksi tuotteen vastaanottotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="2190b-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="2190b-113">Tuotteen vastaanotto 1: määrä = 100 kpl, summa = 1 000,00 €, toimipaikka = 1, varasto =11, eränumero</span><span class="sxs-lookup"><span data-stu-id="2190b-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="2190b-114">= B1</span><span class="sxs-lookup"><span data-stu-id="2190b-114">= B1</span></span>
-   <span data-ttu-id="2190b-115">Tuotteen vastaanotto 2: määrä = 50 kpl, summa = 800,00 €, toimipaikka = 1, varasto =11, eränumero</span><span class="sxs-lookup"><span data-stu-id="2190b-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="2190b-116">= B2</span><span class="sxs-lookup"><span data-stu-id="2190b-116">= B2</span></span>

<span data-ttu-id="2190b-117">Seuraava taulukko sisältää kustannusobjektin laskennan tulokset.</span><span class="sxs-lookup"><span data-stu-id="2190b-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="2190b-118">Voit tarkastella tuloksia **Kustannusobjekti**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2190b-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2190b-119">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="2190b-119">Object type</span></span></th>
<th><span data-ttu-id="2190b-120">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="2190b-120">Item number</span></span></th>
<th><span data-ttu-id="2190b-121">Sivusto</span><span class="sxs-lookup"><span data-stu-id="2190b-121">Site</span></span></th>
<th><span data-ttu-id="2190b-122">Määrä</span><span class="sxs-lookup"><span data-stu-id="2190b-122">Quantity</span></span></th>
<th><span data-ttu-id="2190b-123">Varastoyksikkö</span><span class="sxs-lookup"><span data-stu-id="2190b-123">Inventory unit</span></span></th>
<th><span data-ttu-id="2190b-124">Arvo</span><span class="sxs-lookup"><span data-stu-id="2190b-124">Value</span></span></th>
<th><span data-ttu-id="2190b-125">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="2190b-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2190b-126">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="2190b-126">Cost object</span></span></td>
<td><span data-ttu-id="2190b-127">A</span><span class="sxs-lookup"><span data-stu-id="2190b-127">A</span></span></td>
<td><span data-ttu-id="2190b-128">1</span><span class="sxs-lookup"><span data-stu-id="2190b-128">1</span></span></td>
<td><span data-ttu-id="2190b-129">150</span><span class="sxs-lookup"><span data-stu-id="2190b-129">150</span></span></td>
<td><span data-ttu-id="2190b-130">Kpl.</span><span class="sxs-lookup"><span data-stu-id="2190b-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="2190b-131">1 800,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="2190b-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2190b-133">Seuraava taulukko sisältää varasto-objektin laskennan tulokset.</span><span class="sxs-lookup"><span data-stu-id="2190b-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="2190b-134">Voit tarkastella tuloksia valitsemalla **Kustannusobjekti**-sivun **Fyysinen määrä** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="2190b-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2190b-135">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="2190b-135">Object type</span></span></th>
<th><span data-ttu-id="2190b-136">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="2190b-136">Item number</span></span></th>
<th><span data-ttu-id="2190b-137">Sivusto</span><span class="sxs-lookup"><span data-stu-id="2190b-137">Site</span></span></th>
<th><span data-ttu-id="2190b-138">Varasto</span><span class="sxs-lookup"><span data-stu-id="2190b-138">Warehouse</span></span></th>
<th><span data-ttu-id="2190b-139">Eränumero.</span><span class="sxs-lookup"><span data-stu-id="2190b-139">Batch No.</span></span></th>
<th><span data-ttu-id="2190b-140">Määrä</span><span class="sxs-lookup"><span data-stu-id="2190b-140">Quantity</span></span></th>
<th><span data-ttu-id="2190b-141">Varastoyksikkö</span><span class="sxs-lookup"><span data-stu-id="2190b-141">Inventory unit</span></span></th>
<th><span data-ttu-id="2190b-142">Arvo</span><span class="sxs-lookup"><span data-stu-id="2190b-142">Value</span></span></th>
<th><span data-ttu-id="2190b-143">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="2190b-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2190b-144">Varasto-objekti</span><span class="sxs-lookup"><span data-stu-id="2190b-144">Inventory object</span></span></td>
<td><span data-ttu-id="2190b-145">A</span><span class="sxs-lookup"><span data-stu-id="2190b-145">A</span></span></td>
<td><span data-ttu-id="2190b-146">1</span><span class="sxs-lookup"><span data-stu-id="2190b-146">1</span></span></td>
<td><span data-ttu-id="2190b-147">11</span><span class="sxs-lookup"><span data-stu-id="2190b-147">11</span></span></td>
<td><span data-ttu-id="2190b-148">B1</span><span class="sxs-lookup"><span data-stu-id="2190b-148">B1</span></span></td>
<td><span data-ttu-id="2190b-149">100</span><span class="sxs-lookup"><span data-stu-id="2190b-149">100</span></span></td>
<td><span data-ttu-id="2190b-150">Kpl.</span><span class="sxs-lookup"><span data-stu-id="2190b-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="2190b-151">1 200,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="2190b-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2190b-153">Varasto-objekti</span><span class="sxs-lookup"><span data-stu-id="2190b-153">Inventory object</span></span></td>
<td><span data-ttu-id="2190b-154">A</span><span class="sxs-lookup"><span data-stu-id="2190b-154">A</span></span></td>
<td><span data-ttu-id="2190b-155">1</span><span class="sxs-lookup"><span data-stu-id="2190b-155">1</span></span></td>
<td><span data-ttu-id="2190b-156">11</span><span class="sxs-lookup"><span data-stu-id="2190b-156">11</span></span></td>
<td><span data-ttu-id="2190b-157">B2</span><span class="sxs-lookup"><span data-stu-id="2190b-157">B2</span></span></td>
<td><span data-ttu-id="2190b-158">50</span><span class="sxs-lookup"><span data-stu-id="2190b-158">50</span></span></td>
<td><span data-ttu-id="2190b-159">Kpl.</span><span class="sxs-lookup"><span data-stu-id="2190b-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="2190b-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="2190b-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="2190b-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="2190b-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2190b-162">Additional resources</span></span>
--------

[<span data-ttu-id="2190b-163">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="2190b-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="2190b-164">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="2190b-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="2190b-165">Uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2190b-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]