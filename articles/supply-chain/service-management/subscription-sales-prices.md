---
title: Ylläpitosopimuksen myyntihinnat
description: Kun ylläpitosopimus luodaan, myyntihinta saadaan Myyntihinta (ylläpitosopimus) -lomakkeessa luoduista myyntihinta-asetuksista.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426997"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="b1e70-103">Ylläpitosopimuksen myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="b1e70-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b1e70-104">Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="b1e70-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="b1e70-105">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="b1e70-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="b1e70-106">Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.</span><span class="sxs-lookup"><span data-stu-id="b1e70-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="b1e70-107">Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="b1e70-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="b1e70-108">Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="b1e70-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-109">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="b1e70-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="b1e70-110"><strong>Luokka</strong></span><span class="sxs-lookup"><span data-stu-id="b1e70-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="b1e70-111"><strong>Projektin tunnus</strong></span><span class="sxs-lookup"><span data-stu-id="b1e70-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="b1e70-112"><strong>Ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="b1e70-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="b1e70-113"><strong>Myyntivaluutta</strong></span><span class="sxs-lookup"><span data-stu-id="b1e70-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="b1e70-114"><strong>Kausikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="b1e70-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-115">1</span><span class="sxs-lookup"><span data-stu-id="b1e70-115">1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-116">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-116">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-117">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-117">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-118">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-118">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-119">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-119">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-120">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-121">2</span><span class="sxs-lookup"><span data-stu-id="b1e70-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-122">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-122">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-123">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-123">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-124">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-124">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-125">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-126">3</span><span class="sxs-lookup"><span data-stu-id="b1e70-126">3</span></span></p></td>
<td><p><span data-ttu-id="b1e70-127">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-128">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-128">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-129">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-129">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-130">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-131">4</span><span class="sxs-lookup"><span data-stu-id="b1e70-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-132">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-132">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-133">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-133">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-134">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-135">5</span><span class="sxs-lookup"><span data-stu-id="b1e70-135">5</span></span></p></td>
<td><p><span data-ttu-id="b1e70-136">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-136">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-137">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-138">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-138">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-139">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-140">6</span><span class="sxs-lookup"><span data-stu-id="b1e70-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-141">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-142">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-142">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-143">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-144">7</span><span class="sxs-lookup"><span data-stu-id="b1e70-144">7</span></span></p></td>
<td><p><span data-ttu-id="b1e70-145">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-146">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-146">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-147">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-148">8</span><span class="sxs-lookup"><span data-stu-id="b1e70-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b1e70-149">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-149">X</span></span></p></td>
<td><p><span data-ttu-id="b1e70-150">X</span><span class="sxs-lookup"><span data-stu-id="b1e70-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-151">Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.</span><span class="sxs-lookup"><span data-stu-id="b1e70-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="b1e70-152">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="b1e70-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="b1e70-153">Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin.</span><span class="sxs-lookup"><span data-stu-id="b1e70-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="b1e70-154">Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.</span><span class="sxs-lookup"><span data-stu-id="b1e70-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="b1e70-155">Ylläpitosopimusmaksun myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="b1e70-155">Subscription fee sales prices</span></span>

<span data-ttu-id="b1e70-156">Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="b1e70-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="b1e70-157">Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="b1e70-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="b1e70-158">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="b1e70-158">Example</span></span>

<span data-ttu-id="b1e70-159">Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="b1e70-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="b1e70-160">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b1e70-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-161">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="b1e70-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="b1e70-162">Luokka</span><span class="sxs-lookup"><span data-stu-id="b1e70-162">Category</span></span></p></th>
<th><p><span data-ttu-id="b1e70-163">Project</span><span class="sxs-lookup"><span data-stu-id="b1e70-163">Project</span></span></p></th>
<th><p><span data-ttu-id="b1e70-164">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b1e70-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b1e70-165">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="b1e70-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="b1e70-166">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="b1e70-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b1e70-167">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b1e70-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-168">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="b1e70-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1e70-169">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1e70-170">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="b1e70-170">Month</span></span></p></td>
<td><p><span data-ttu-id="b1e70-171">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-172">500</span><span class="sxs-lookup"><span data-stu-id="b1e70-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-173">Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="b1e70-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="b1e70-174">Sitten luot seuraavat ylläpitosopimukset.</span><span class="sxs-lookup"><span data-stu-id="b1e70-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-175">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b1e70-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="b1e70-176">Project</span><span class="sxs-lookup"><span data-stu-id="b1e70-176">Project</span></span></p></th>
<th><p><span data-ttu-id="b1e70-177">Ylläpitosopimusryhmä</span><span class="sxs-lookup"><span data-stu-id="b1e70-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="b1e70-178">Luokka</span><span class="sxs-lookup"><span data-stu-id="b1e70-178">Category</span></span></p></th>
<th><p><span data-ttu-id="b1e70-179">Valuutta</span><span class="sxs-lookup"><span data-stu-id="b1e70-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="b1e70-180">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="b1e70-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-182">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-182">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="b1e70-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="b1e70-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-185">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-186">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="b1e70-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-188">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-188">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="b1e70-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b1e70-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b1e70-191">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-192">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="b1e70-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-193">Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:</span><span class="sxs-lookup"><span data-stu-id="b1e70-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="b1e70-194">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="b1e70-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="b1e70-195">Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="b1e70-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="b1e70-196">Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="b1e70-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="b1e70-197">Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b1e70-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="b1e70-198">Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b1e70-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-199">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="b1e70-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-200">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b1e70-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="b1e70-201">Project</span><span class="sxs-lookup"><span data-stu-id="b1e70-201">Project</span></span></p></th>
<th><p><span data-ttu-id="b1e70-202">Luokka</span><span class="sxs-lookup"><span data-stu-id="b1e70-202">Category</span></span></p></th>
<th><p><span data-ttu-id="b1e70-203">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="b1e70-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-204">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="b1e70-204">End date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-205">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="b1e70-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b1e70-206">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b1e70-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-207">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="b1e70-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="b1e70-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-209">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-209">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="b1e70-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-211">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-212">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-213">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-214">500</span><span class="sxs-lookup"><span data-stu-id="b1e70-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-215">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="b1e70-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="b1e70-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-217">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-217">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b1e70-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b1e70-219">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-220">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-221">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-222">500</span><span class="sxs-lookup"><span data-stu-id="b1e70-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-223">Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030.</span><span class="sxs-lookup"><span data-stu-id="b1e70-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="b1e70-224">Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="b1e70-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="b1e70-225">Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b1e70-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-226">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="b1e70-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="b1e70-227">Luokka</span><span class="sxs-lookup"><span data-stu-id="b1e70-227">Category</span></span></p></th>
<th><p><span data-ttu-id="b1e70-228">Project</span><span class="sxs-lookup"><span data-stu-id="b1e70-228">Project</span></span></p></th>
<th><p><span data-ttu-id="b1e70-229">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b1e70-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b1e70-230">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="b1e70-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="b1e70-231">Valuutta</span><span class="sxs-lookup"><span data-stu-id="b1e70-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="b1e70-232">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b1e70-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-233">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1e70-234">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1e70-235">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="b1e70-235">Month</span></span></p></td>
<td><p><span data-ttu-id="b1e70-236">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-237">500</span><span class="sxs-lookup"><span data-stu-id="b1e70-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-238">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="b1e70-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-240">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b1e70-241">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="b1e70-241">Month</span></span></p></td>
<td><p><span data-ttu-id="b1e70-242">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-243">550</span><span class="sxs-lookup"><span data-stu-id="b1e70-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-244">Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="b1e70-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="b1e70-245">Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.</span><span class="sxs-lookup"><span data-stu-id="b1e70-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1e70-246">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="b1e70-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-247">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b1e70-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b1e70-248">Project</span><span class="sxs-lookup"><span data-stu-id="b1e70-248">Project</span></span></p></th>
<th><p><span data-ttu-id="b1e70-249">Luokka</span><span class="sxs-lookup"><span data-stu-id="b1e70-249">Category</span></span></p></th>
<th><p><span data-ttu-id="b1e70-250">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="b1e70-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-251">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="b1e70-251">End date</span></span></p></th>
<th><p><span data-ttu-id="b1e70-252">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="b1e70-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b1e70-253">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b1e70-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1e70-254">28.7.2007</span><span class="sxs-lookup"><span data-stu-id="b1e70-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="b1e70-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-256">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-256">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="b1e70-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="b1e70-258">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="b1e70-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="b1e70-259">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="b1e70-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="b1e70-260">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-261">550</span><span class="sxs-lookup"><span data-stu-id="b1e70-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1e70-262">28.7.2008</span><span class="sxs-lookup"><span data-stu-id="b1e70-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="b1e70-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="b1e70-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="b1e70-264">9030</span><span class="sxs-lookup"><span data-stu-id="b1e70-264">9030</span></span></p></td>
<td><p><span data-ttu-id="b1e70-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b1e70-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b1e70-266">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="b1e70-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="b1e70-267">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="b1e70-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="b1e70-268">Euro</span><span class="sxs-lookup"><span data-stu-id="b1e70-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="b1e70-269">500</span><span class="sxs-lookup"><span data-stu-id="b1e70-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1e70-270">Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta.</span><span class="sxs-lookup"><span data-stu-id="b1e70-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="b1e70-271">Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.</span><span class="sxs-lookup"><span data-stu-id="b1e70-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1e70-272">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="b1e70-272">See also</span></span>

[<span data-ttu-id="b1e70-273">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="b1e70-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


