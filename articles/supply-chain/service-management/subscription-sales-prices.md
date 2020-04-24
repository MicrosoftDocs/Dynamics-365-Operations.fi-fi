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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c59c90d49a4dcf3df4672c5f40d52ed639760c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206608"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="6c0fc-103">Ylläpitosopimuksen myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="6c0fc-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c0fc-104">Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="6c0fc-105">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="6c0fc-106">Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="6c0fc-107">Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="6c0fc-108">Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="6c0fc-109">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="6c0fc-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-110"><strong>Luokka</strong></span><span class="sxs-lookup"><span data-stu-id="6c0fc-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="6c0fc-111"><strong>Projektin tunnus</strong></span><span class="sxs-lookup"><span data-stu-id="6c0fc-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="6c0fc-112"><strong>Ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="6c0fc-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="6c0fc-113"><strong>Myyntivaluutta</strong></span><span class="sxs-lookup"><span data-stu-id="6c0fc-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="6c0fc-114"><strong>Kausikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="6c0fc-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-115">1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-115">1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-116">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-116">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-117">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-117">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-118">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-118">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-119">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-119">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-120">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-121">2</span><span class="sxs-lookup"><span data-stu-id="6c0fc-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-122">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-122">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-123">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-123">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-124">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-124">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-125">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-126">3</span><span class="sxs-lookup"><span data-stu-id="6c0fc-126">3</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-127">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-128">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-128">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-129">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-129">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-130">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-131">4</span><span class="sxs-lookup"><span data-stu-id="6c0fc-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-132">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-132">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-133">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-133">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-134">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-135">5</span><span class="sxs-lookup"><span data-stu-id="6c0fc-135">5</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-136">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-136">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-137">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-138">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-138">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-139">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-140">6</span><span class="sxs-lookup"><span data-stu-id="6c0fc-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-141">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-142">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-142">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-143">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-144">7</span><span class="sxs-lookup"><span data-stu-id="6c0fc-144">7</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-145">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-146">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-146">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-147">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-148">8</span><span class="sxs-lookup"><span data-stu-id="6c0fc-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c0fc-149">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-149">X</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-150">X</span><span class="sxs-lookup"><span data-stu-id="6c0fc-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-151">Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="6c0fc-152">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="6c0fc-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="6c0fc-153">Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="6c0fc-154">Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="6c0fc-155">Ylläpitosopimusmaksun myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="6c0fc-155">Subscription fee sales prices</span></span>

<span data-ttu-id="6c0fc-156">Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="6c0fc-157">Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="6c0fc-158">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6c0fc-158">Example</span></span>

<span data-ttu-id="6c0fc-159">Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="6c0fc-160">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="6c0fc-161">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="6c0fc-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-162">Luokka</span><span class="sxs-lookup"><span data-stu-id="6c0fc-162">Category</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-163">Project</span><span class="sxs-lookup"><span data-stu-id="6c0fc-163">Project</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-164">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="6c0fc-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-165">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-166">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-167">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-168">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="6c0fc-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c0fc-169">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c0fc-170">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-170">Month</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-171">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-172">500</span><span class="sxs-lookup"><span data-stu-id="6c0fc-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-173">Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="6c0fc-174">Sitten luot seuraavat ylläpitosopimukset.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="6c0fc-175">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="6c0fc-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-176">Project</span><span class="sxs-lookup"><span data-stu-id="6c0fc-176">Project</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-177">Ylläpitosopimusryhmä</span><span class="sxs-lookup"><span data-stu-id="6c0fc-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-178">Luokka</span><span class="sxs-lookup"><span data-stu-id="6c0fc-178">Category</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-179">Valuutta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-180">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-182">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-182">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-185">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-186">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="6c0fc-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-188">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-188">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="6c0fc-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-191">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-192">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="6c0fc-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-193">Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:</span><span class="sxs-lookup"><span data-stu-id="6c0fc-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="6c0fc-194">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="6c0fc-195">Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="6c0fc-196">Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="6c0fc-197">Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6c0fc-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="6c0fc-198">Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c0fc-199">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="6c0fc-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-200">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="6c0fc-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-201">Project</span><span class="sxs-lookup"><span data-stu-id="6c0fc-201">Project</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-202">Luokka</span><span class="sxs-lookup"><span data-stu-id="6c0fc-202">Category</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-203">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6c0fc-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-204">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="6c0fc-204">End date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-205">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-206">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-207">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="6c0fc-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-209">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-209">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-211">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-212">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-213">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-214">500</span><span class="sxs-lookup"><span data-stu-id="6c0fc-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-215">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="6c0fc-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-217">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-217">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="6c0fc-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-219">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-220">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-221">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-222">500</span><span class="sxs-lookup"><span data-stu-id="6c0fc-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-223">Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="6c0fc-224">Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="6c0fc-225">Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c0fc-226">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="6c0fc-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-227">Luokka</span><span class="sxs-lookup"><span data-stu-id="6c0fc-227">Category</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-228">Project</span><span class="sxs-lookup"><span data-stu-id="6c0fc-228">Project</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-229">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="6c0fc-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-230">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-231">Valuutta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-232">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-233">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c0fc-234">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c0fc-235">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-235">Month</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-236">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-237">500</span><span class="sxs-lookup"><span data-stu-id="6c0fc-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-238">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-240">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c0fc-241">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="6c0fc-241">Month</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-242">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-243">550</span><span class="sxs-lookup"><span data-stu-id="6c0fc-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-244">Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="6c0fc-245">Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="6c0fc-246">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="6c0fc-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-247">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="6c0fc-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-248">Project</span><span class="sxs-lookup"><span data-stu-id="6c0fc-248">Project</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-249">Luokka</span><span class="sxs-lookup"><span data-stu-id="6c0fc-249">Category</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-250">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6c0fc-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-251">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6c0fc-251">End date</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-252">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c0fc-253">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="6c0fc-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0fc-254">28.7.2007</span><span class="sxs-lookup"><span data-stu-id="6c0fc-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-256">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-256">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="6c0fc-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-258">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="6c0fc-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-259">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="6c0fc-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-260">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-261">550</span><span class="sxs-lookup"><span data-stu-id="6c0fc-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0fc-262">28.7.2008</span><span class="sxs-lookup"><span data-stu-id="6c0fc-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c0fc-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-264">9030</span><span class="sxs-lookup"><span data-stu-id="6c0fc-264">9030</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="6c0fc-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-266">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="6c0fc-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-267">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="6c0fc-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-268">Euro</span><span class="sxs-lookup"><span data-stu-id="6c0fc-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c0fc-269">500</span><span class="sxs-lookup"><span data-stu-id="6c0fc-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c0fc-270">Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="6c0fc-271">Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.</span><span class="sxs-lookup"><span data-stu-id="6c0fc-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c0fc-272">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6c0fc-272">See also</span></span>

[<span data-ttu-id="6c0fc-273">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="6c0fc-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


