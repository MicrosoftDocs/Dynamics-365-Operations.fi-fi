---
title: Ylläpitosopimuksen myyntihinnat
description: Kun ylläpitosopimus luodaan, myyntihinta saadaan Myyntihinta (ylläpitosopimus) -lomakkeessa luoduista myyntihinta-asetuksista.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4b02af0a535e67818751c437482c3663524474
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817410"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="16624-103">Ylläpitosopimuksen myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="16624-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="16624-104">Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="16624-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="16624-105">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="16624-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="16624-106">Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.</span><span class="sxs-lookup"><span data-stu-id="16624-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="16624-107">Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="16624-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="16624-108">Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="16624-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="16624-109">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="16624-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="16624-110"><strong>Luokka</strong></span><span class="sxs-lookup"><span data-stu-id="16624-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="16624-111"><strong>Projektin tunnus</strong></span><span class="sxs-lookup"><span data-stu-id="16624-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="16624-112"><strong>Ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="16624-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="16624-113"><strong>Myyntivaluutta</strong></span><span class="sxs-lookup"><span data-stu-id="16624-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="16624-114"><strong>Kausikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="16624-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-115">1</span><span class="sxs-lookup"><span data-stu-id="16624-115">1</span></span></p></td>
<td><p><span data-ttu-id="16624-116">X</span><span class="sxs-lookup"><span data-stu-id="16624-116">X</span></span></p></td>
<td><p><span data-ttu-id="16624-117">X</span><span class="sxs-lookup"><span data-stu-id="16624-117">X</span></span></p></td>
<td><p><span data-ttu-id="16624-118">X</span><span class="sxs-lookup"><span data-stu-id="16624-118">X</span></span></p></td>
<td><p><span data-ttu-id="16624-119">X</span><span class="sxs-lookup"><span data-stu-id="16624-119">X</span></span></p></td>
<td><p><span data-ttu-id="16624-120">X</span><span class="sxs-lookup"><span data-stu-id="16624-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-121">2</span><span class="sxs-lookup"><span data-stu-id="16624-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-122">X</span><span class="sxs-lookup"><span data-stu-id="16624-122">X</span></span></p></td>
<td><p><span data-ttu-id="16624-123">X</span><span class="sxs-lookup"><span data-stu-id="16624-123">X</span></span></p></td>
<td><p><span data-ttu-id="16624-124">X</span><span class="sxs-lookup"><span data-stu-id="16624-124">X</span></span></p></td>
<td><p><span data-ttu-id="16624-125">X</span><span class="sxs-lookup"><span data-stu-id="16624-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16624-126">3</span><span class="sxs-lookup"><span data-stu-id="16624-126">3</span></span></p></td>
<td><p><span data-ttu-id="16624-127">X</span><span class="sxs-lookup"><span data-stu-id="16624-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-128">X</span><span class="sxs-lookup"><span data-stu-id="16624-128">X</span></span></p></td>
<td><p><span data-ttu-id="16624-129">X</span><span class="sxs-lookup"><span data-stu-id="16624-129">X</span></span></p></td>
<td><p><span data-ttu-id="16624-130">X</span><span class="sxs-lookup"><span data-stu-id="16624-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-131">4</span><span class="sxs-lookup"><span data-stu-id="16624-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-132">X</span><span class="sxs-lookup"><span data-stu-id="16624-132">X</span></span></p></td>
<td><p><span data-ttu-id="16624-133">X</span><span class="sxs-lookup"><span data-stu-id="16624-133">X</span></span></p></td>
<td><p><span data-ttu-id="16624-134">X</span><span class="sxs-lookup"><span data-stu-id="16624-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16624-135">5</span><span class="sxs-lookup"><span data-stu-id="16624-135">5</span></span></p></td>
<td><p><span data-ttu-id="16624-136">X</span><span class="sxs-lookup"><span data-stu-id="16624-136">X</span></span></p></td>
<td><p><span data-ttu-id="16624-137">X</span><span class="sxs-lookup"><span data-stu-id="16624-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-138">X</span><span class="sxs-lookup"><span data-stu-id="16624-138">X</span></span></p></td>
<td><p><span data-ttu-id="16624-139">X</span><span class="sxs-lookup"><span data-stu-id="16624-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-140">6</span><span class="sxs-lookup"><span data-stu-id="16624-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-141">X</span><span class="sxs-lookup"><span data-stu-id="16624-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-142">X</span><span class="sxs-lookup"><span data-stu-id="16624-142">X</span></span></p></td>
<td><p><span data-ttu-id="16624-143">X</span><span class="sxs-lookup"><span data-stu-id="16624-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16624-144">7</span><span class="sxs-lookup"><span data-stu-id="16624-144">7</span></span></p></td>
<td><p><span data-ttu-id="16624-145">X</span><span class="sxs-lookup"><span data-stu-id="16624-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-146">X</span><span class="sxs-lookup"><span data-stu-id="16624-146">X</span></span></p></td>
<td><p><span data-ttu-id="16624-147">X</span><span class="sxs-lookup"><span data-stu-id="16624-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-148">8</span><span class="sxs-lookup"><span data-stu-id="16624-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="16624-149">X</span><span class="sxs-lookup"><span data-stu-id="16624-149">X</span></span></p></td>
<td><p><span data-ttu-id="16624-150">X</span><span class="sxs-lookup"><span data-stu-id="16624-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-151">Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.</span><span class="sxs-lookup"><span data-stu-id="16624-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="16624-152">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="16624-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="16624-153">Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin.</span><span class="sxs-lookup"><span data-stu-id="16624-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="16624-154">Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.</span><span class="sxs-lookup"><span data-stu-id="16624-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="16624-155">Ylläpitosopimusmaksun myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="16624-155">Subscription fee sales prices</span></span>

<span data-ttu-id="16624-156">Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="16624-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="16624-157">Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="16624-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="16624-158">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="16624-158">Example</span></span>

<span data-ttu-id="16624-159">Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="16624-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="16624-160">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="16624-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="16624-161">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="16624-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="16624-162">Luokka</span><span class="sxs-lookup"><span data-stu-id="16624-162">Category</span></span></p></th>
<th><p><span data-ttu-id="16624-163">Project</span><span class="sxs-lookup"><span data-stu-id="16624-163">Project</span></span></p></th>
<th><p><span data-ttu-id="16624-164">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="16624-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="16624-165">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="16624-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="16624-166">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="16624-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="16624-167">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="16624-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-168">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="16624-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="16624-169">9030</span><span class="sxs-lookup"><span data-stu-id="16624-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="16624-170">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="16624-170">Month</span></span></p></td>
<td><p><span data-ttu-id="16624-171">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-172">500</span><span class="sxs-lookup"><span data-stu-id="16624-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-173">Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="16624-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="16624-174">Sitten luot seuraavat ylläpitosopimukset.</span><span class="sxs-lookup"><span data-stu-id="16624-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="16624-175">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="16624-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="16624-176">Project</span><span class="sxs-lookup"><span data-stu-id="16624-176">Project</span></span></p></th>
<th><p><span data-ttu-id="16624-177">Ylläpitosopimusryhmä</span><span class="sxs-lookup"><span data-stu-id="16624-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="16624-178">Luokka</span><span class="sxs-lookup"><span data-stu-id="16624-178">Category</span></span></p></th>
<th><p><span data-ttu-id="16624-179">Valuutta</span><span class="sxs-lookup"><span data-stu-id="16624-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="16624-180">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="16624-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="16624-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="16624-182">9030</span><span class="sxs-lookup"><span data-stu-id="16624-182">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="16624-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="16624-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="16624-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="16624-185">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-186">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="16624-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="16624-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="16624-188">9030</span><span class="sxs-lookup"><span data-stu-id="16624-188">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="16624-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="16624-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="16624-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="16624-191">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-192">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="16624-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-193">Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:</span><span class="sxs-lookup"><span data-stu-id="16624-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="16624-194">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="16624-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="16624-195">Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="16624-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="16624-196">Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="16624-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="16624-197">Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="16624-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="16624-198">Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="16624-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="16624-199">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="16624-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="16624-200">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="16624-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="16624-201">Project</span><span class="sxs-lookup"><span data-stu-id="16624-201">Project</span></span></p></th>
<th><p><span data-ttu-id="16624-202">Luokka</span><span class="sxs-lookup"><span data-stu-id="16624-202">Category</span></span></p></th>
<th><p><span data-ttu-id="16624-203">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="16624-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="16624-204">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="16624-204">End date</span></span></p></th>
<th><p><span data-ttu-id="16624-205">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="16624-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="16624-206">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="16624-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-207">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="16624-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="16624-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="16624-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="16624-209">9030</span><span class="sxs-lookup"><span data-stu-id="16624-209">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="16624-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="16624-211">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="16624-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-212">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="16624-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-213">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-214">500</span><span class="sxs-lookup"><span data-stu-id="16624-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-215">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="16624-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="16624-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="16624-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="16624-217">9030</span><span class="sxs-lookup"><span data-stu-id="16624-217">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="16624-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="16624-219">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="16624-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-220">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="16624-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-221">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-222">500</span><span class="sxs-lookup"><span data-stu-id="16624-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-223">Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030.</span><span class="sxs-lookup"><span data-stu-id="16624-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="16624-224">Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="16624-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="16624-225">Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="16624-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="16624-226">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="16624-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="16624-227">Luokka</span><span class="sxs-lookup"><span data-stu-id="16624-227">Category</span></span></p></th>
<th><p><span data-ttu-id="16624-228">Project</span><span class="sxs-lookup"><span data-stu-id="16624-228">Project</span></span></p></th>
<th><p><span data-ttu-id="16624-229">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="16624-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="16624-230">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="16624-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="16624-231">Valuutta</span><span class="sxs-lookup"><span data-stu-id="16624-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="16624-232">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="16624-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-233">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="16624-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="16624-234">9030</span><span class="sxs-lookup"><span data-stu-id="16624-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="16624-235">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="16624-235">Month</span></span></p></td>
<td><p><span data-ttu-id="16624-236">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-237">500</span><span class="sxs-lookup"><span data-stu-id="16624-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-238">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="16624-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="16624-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="16624-240">9030</span><span class="sxs-lookup"><span data-stu-id="16624-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="16624-241">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="16624-241">Month</span></span></p></td>
<td><p><span data-ttu-id="16624-242">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-243">550</span><span class="sxs-lookup"><span data-stu-id="16624-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-244">Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="16624-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="16624-245">Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.</span><span class="sxs-lookup"><span data-stu-id="16624-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="16624-246">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="16624-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="16624-247">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="16624-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="16624-248">Project</span><span class="sxs-lookup"><span data-stu-id="16624-248">Project</span></span></p></th>
<th><p><span data-ttu-id="16624-249">Luokka</span><span class="sxs-lookup"><span data-stu-id="16624-249">Category</span></span></p></th>
<th><p><span data-ttu-id="16624-250">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="16624-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="16624-251">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="16624-251">End date</span></span></p></th>
<th><p><span data-ttu-id="16624-252">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="16624-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="16624-253">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="16624-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16624-254">28.7.2007</span><span class="sxs-lookup"><span data-stu-id="16624-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="16624-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="16624-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="16624-256">9030</span><span class="sxs-lookup"><span data-stu-id="16624-256">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="16624-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="16624-258">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="16624-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="16624-259">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="16624-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="16624-260">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-261">550</span><span class="sxs-lookup"><span data-stu-id="16624-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16624-262">28.7.2008</span><span class="sxs-lookup"><span data-stu-id="16624-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="16624-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="16624-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="16624-264">9030</span><span class="sxs-lookup"><span data-stu-id="16624-264">9030</span></span></p></td>
<td><p><span data-ttu-id="16624-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="16624-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="16624-266">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="16624-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="16624-267">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="16624-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="16624-268">Euro</span><span class="sxs-lookup"><span data-stu-id="16624-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="16624-269">500</span><span class="sxs-lookup"><span data-stu-id="16624-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16624-270">Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta.</span><span class="sxs-lookup"><span data-stu-id="16624-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="16624-271">Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.</span><span class="sxs-lookup"><span data-stu-id="16624-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="16624-272">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="16624-272">See also</span></span>

[<span data-ttu-id="16624-273">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="16624-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]