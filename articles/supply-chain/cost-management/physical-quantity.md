---
title: Varasto-objektin arvot
description: Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "319129"
---
# <a name="inventory-object-values"></a><span data-ttu-id="f9b1a-103">Varasto-objektin arvot</span><span class="sxs-lookup"><span data-stu-id="f9b1a-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9b1a-104">Tässä artikkelissa on tietoja siitä, miten varasto-objektien arvot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="f9b1a-105">**Fyysinen määrä**-nimisen uuden toiminnon avulla näet tietyn varasto-objektin arvot.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="f9b1a-106">Kustannusobjekti edustaa sen yksikön tasoa, jolla varaston kirjanpito suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="f9b1a-107">Lisätietoja kustannusobjekteista on kohdassa [Kustannusobjektit](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="f9b1a-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="f9b1a-108">Saat tietyn varasto-objektin arvot näkyviin valitsemalla **Fyysinen määrä** **Kustannusobjekti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="f9b1a-109">Varasto-objektin arvo lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f9b1a-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="f9b1a-110">Varasto-objekti.Arvo = Kustannusobjekti.Keskimääräinen yksikkökustannus × Varasto-objekti.Määrä</span><span class="sxs-lookup"><span data-stu-id="f9b1a-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="f9b1a-111">Seuraavassa esimerkissä näytetään, miten varasto-objektin ja kustannusobjektin arvot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="f9b1a-112">Nimikkeelle A on rekisteröity kaksi tuotteen vastaanottotapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="f9b1a-113">Tuotteen vastaanotto 1: määrä = 100 kpl, summa = 1 000,00 €, toimipaikka = 1, varasto =11, eränumero</span><span class="sxs-lookup"><span data-stu-id="f9b1a-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="f9b1a-114">= B1</span><span class="sxs-lookup"><span data-stu-id="f9b1a-114">= B1</span></span>
-   <span data-ttu-id="f9b1a-115">Tuotteen vastaanotto 2: määrä = 50 kpl, summa = 800,00 €, toimipaikka = 1, varasto =11, eränumero</span><span class="sxs-lookup"><span data-stu-id="f9b1a-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="f9b1a-116">= B2</span><span class="sxs-lookup"><span data-stu-id="f9b1a-116">= B2</span></span>

<span data-ttu-id="f9b1a-117">Seuraava taulukko sisältää kustannusobjektin laskennan tulokset.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="f9b1a-118">Voit tarkastella tuloksia **Kustannusobjekti**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="f9b1a-119">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="f9b1a-119">Object type</span></span></th>
<th><span data-ttu-id="f9b1a-120">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="f9b1a-120">Item number</span></span></th>
<th><span data-ttu-id="f9b1a-121">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f9b1a-121">Site</span></span></th>
<th><span data-ttu-id="f9b1a-122">Määrä</span><span class="sxs-lookup"><span data-stu-id="f9b1a-122">Quantity</span></span></th>
<th><span data-ttu-id="f9b1a-123">Varastoyksikkö</span><span class="sxs-lookup"><span data-stu-id="f9b1a-123">Inventory unit</span></span></th>
<th><span data-ttu-id="f9b1a-124">Arvo</span><span class="sxs-lookup"><span data-stu-id="f9b1a-124">Value</span></span></th>
<th><span data-ttu-id="f9b1a-125">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="f9b1a-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9b1a-126">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="f9b1a-126">Cost object</span></span></td>
<td><span data-ttu-id="f9b1a-127">A</span><span class="sxs-lookup"><span data-stu-id="f9b1a-127">A</span></span></td>
<td><span data-ttu-id="f9b1a-128">1</span><span class="sxs-lookup"><span data-stu-id="f9b1a-128">1</span></span></td>
<td><span data-ttu-id="f9b1a-129">150</span><span class="sxs-lookup"><span data-stu-id="f9b1a-129">150</span></span></td>
<td><span data-ttu-id="f9b1a-130">Kpl.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="f9b1a-131">1 800,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="f9b1a-132">12,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9b1a-133">Seuraava taulukko sisältää varasto-objektin laskennan tulokset.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="f9b1a-134">Voit tarkastella tuloksia valitsemalla **Kustannusobjekti**-sivun **Fyysinen määrä** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="f9b1a-135">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="f9b1a-135">Object type</span></span></th>
<th><span data-ttu-id="f9b1a-136">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="f9b1a-136">Item number</span></span></th>
<th><span data-ttu-id="f9b1a-137">Sivusto</span><span class="sxs-lookup"><span data-stu-id="f9b1a-137">Site</span></span></th>
<th><span data-ttu-id="f9b1a-138">Varasto</span><span class="sxs-lookup"><span data-stu-id="f9b1a-138">Warehouse</span></span></th>
<th><span data-ttu-id="f9b1a-139">Eränumero.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-139">Batch No.</span></span></th>
<th><span data-ttu-id="f9b1a-140">Määrä</span><span class="sxs-lookup"><span data-stu-id="f9b1a-140">Quantity</span></span></th>
<th><span data-ttu-id="f9b1a-141">Varastoyksikkö</span><span class="sxs-lookup"><span data-stu-id="f9b1a-141">Inventory unit</span></span></th>
<th><span data-ttu-id="f9b1a-142">Arvo</span><span class="sxs-lookup"><span data-stu-id="f9b1a-142">Value</span></span></th>
<th><span data-ttu-id="f9b1a-143">Keskimääräinen yksikkökustannus</span><span class="sxs-lookup"><span data-stu-id="f9b1a-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9b1a-144">Varasto-objekti</span><span class="sxs-lookup"><span data-stu-id="f9b1a-144">Inventory object</span></span></td>
<td><span data-ttu-id="f9b1a-145">A</span><span class="sxs-lookup"><span data-stu-id="f9b1a-145">A</span></span></td>
<td><span data-ttu-id="f9b1a-146">1</span><span class="sxs-lookup"><span data-stu-id="f9b1a-146">1</span></span></td>
<td><span data-ttu-id="f9b1a-147">11</span><span class="sxs-lookup"><span data-stu-id="f9b1a-147">11</span></span></td>
<td><span data-ttu-id="f9b1a-148">B1</span><span class="sxs-lookup"><span data-stu-id="f9b1a-148">B1</span></span></td>
<td><span data-ttu-id="f9b1a-149">100</span><span class="sxs-lookup"><span data-stu-id="f9b1a-149">100</span></span></td>
<td><span data-ttu-id="f9b1a-150">Kpl.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="f9b1a-151">1 200,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="f9b1a-152">12,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b1a-153">Varasto-objekti</span><span class="sxs-lookup"><span data-stu-id="f9b1a-153">Inventory object</span></span></td>
<td><span data-ttu-id="f9b1a-154">A</span><span class="sxs-lookup"><span data-stu-id="f9b1a-154">A</span></span></td>
<td><span data-ttu-id="f9b1a-155">1</span><span class="sxs-lookup"><span data-stu-id="f9b1a-155">1</span></span></td>
<td><span data-ttu-id="f9b1a-156">11</span><span class="sxs-lookup"><span data-stu-id="f9b1a-156">11</span></span></td>
<td><span data-ttu-id="f9b1a-157">B2</span><span class="sxs-lookup"><span data-stu-id="f9b1a-157">B2</span></span></td>
<td><span data-ttu-id="f9b1a-158">50</span><span class="sxs-lookup"><span data-stu-id="f9b1a-158">50</span></span></td>
<td><span data-ttu-id="f9b1a-159">Kpl.</span><span class="sxs-lookup"><span data-stu-id="f9b1a-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="f9b1a-160">600,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="f9b1a-161">12,00 €</span><span class="sxs-lookup"><span data-stu-id="f9b1a-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="f9b1a-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f9b1a-162">Additional resources</span></span>
--------

[<span data-ttu-id="f9b1a-163">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="f9b1a-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="f9b1a-164">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="f9b1a-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="f9b1a-165">Uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f9b1a-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



