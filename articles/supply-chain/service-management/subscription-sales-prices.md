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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974208"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="2d234-103">Ylläpitosopimuksen myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="2d234-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2d234-104">Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="2d234-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="2d234-105">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="2d234-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="2d234-106">Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.</span><span class="sxs-lookup"><span data-stu-id="2d234-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="2d234-107">Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="2d234-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="2d234-108">Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="2d234-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="2d234-109">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="2d234-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="2d234-110"><strong>Luokka</strong></span><span class="sxs-lookup"><span data-stu-id="2d234-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="2d234-111"><strong>Projektin tunnus</strong></span><span class="sxs-lookup"><span data-stu-id="2d234-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="2d234-112"><strong>Ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="2d234-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="2d234-113"><strong>Myyntivaluutta</strong></span><span class="sxs-lookup"><span data-stu-id="2d234-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="2d234-114"><strong>Kausikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="2d234-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-115">1</span><span class="sxs-lookup"><span data-stu-id="2d234-115">1</span></span></p></td>
<td><p><span data-ttu-id="2d234-116">X</span><span class="sxs-lookup"><span data-stu-id="2d234-116">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-117">X</span><span class="sxs-lookup"><span data-stu-id="2d234-117">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-118">X</span><span class="sxs-lookup"><span data-stu-id="2d234-118">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-119">X</span><span class="sxs-lookup"><span data-stu-id="2d234-119">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-120">X</span><span class="sxs-lookup"><span data-stu-id="2d234-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-121">2</span><span class="sxs-lookup"><span data-stu-id="2d234-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-122">X</span><span class="sxs-lookup"><span data-stu-id="2d234-122">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-123">X</span><span class="sxs-lookup"><span data-stu-id="2d234-123">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-124">X</span><span class="sxs-lookup"><span data-stu-id="2d234-124">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-125">X</span><span class="sxs-lookup"><span data-stu-id="2d234-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d234-126">3</span><span class="sxs-lookup"><span data-stu-id="2d234-126">3</span></span></p></td>
<td><p><span data-ttu-id="2d234-127">X</span><span class="sxs-lookup"><span data-stu-id="2d234-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-128">X</span><span class="sxs-lookup"><span data-stu-id="2d234-128">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-129">X</span><span class="sxs-lookup"><span data-stu-id="2d234-129">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-130">X</span><span class="sxs-lookup"><span data-stu-id="2d234-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-131">4</span><span class="sxs-lookup"><span data-stu-id="2d234-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-132">X</span><span class="sxs-lookup"><span data-stu-id="2d234-132">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-133">X</span><span class="sxs-lookup"><span data-stu-id="2d234-133">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-134">X</span><span class="sxs-lookup"><span data-stu-id="2d234-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d234-135">5</span><span class="sxs-lookup"><span data-stu-id="2d234-135">5</span></span></p></td>
<td><p><span data-ttu-id="2d234-136">X</span><span class="sxs-lookup"><span data-stu-id="2d234-136">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-137">X</span><span class="sxs-lookup"><span data-stu-id="2d234-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-138">X</span><span class="sxs-lookup"><span data-stu-id="2d234-138">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-139">X</span><span class="sxs-lookup"><span data-stu-id="2d234-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-140">6</span><span class="sxs-lookup"><span data-stu-id="2d234-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-141">X</span><span class="sxs-lookup"><span data-stu-id="2d234-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-142">X</span><span class="sxs-lookup"><span data-stu-id="2d234-142">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-143">X</span><span class="sxs-lookup"><span data-stu-id="2d234-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d234-144">7</span><span class="sxs-lookup"><span data-stu-id="2d234-144">7</span></span></p></td>
<td><p><span data-ttu-id="2d234-145">X</span><span class="sxs-lookup"><span data-stu-id="2d234-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-146">X</span><span class="sxs-lookup"><span data-stu-id="2d234-146">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-147">X</span><span class="sxs-lookup"><span data-stu-id="2d234-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-148">8</span><span class="sxs-lookup"><span data-stu-id="2d234-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2d234-149">X</span><span class="sxs-lookup"><span data-stu-id="2d234-149">X</span></span></p></td>
<td><p><span data-ttu-id="2d234-150">X</span><span class="sxs-lookup"><span data-stu-id="2d234-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-151">Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.</span><span class="sxs-lookup"><span data-stu-id="2d234-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="2d234-152">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="2d234-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="2d234-153">Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin.</span><span class="sxs-lookup"><span data-stu-id="2d234-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="2d234-154">Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.</span><span class="sxs-lookup"><span data-stu-id="2d234-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="2d234-155">Ylläpitosopimusmaksun myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="2d234-155">Subscription fee sales prices</span></span>

<span data-ttu-id="2d234-156">Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="2d234-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="2d234-157">Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="2d234-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="2d234-158">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="2d234-158">Example</span></span>

<span data-ttu-id="2d234-159">Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="2d234-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="2d234-160">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="2d234-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="2d234-161">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="2d234-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2d234-162">Luokka</span><span class="sxs-lookup"><span data-stu-id="2d234-162">Category</span></span></p></th>
<th><p><span data-ttu-id="2d234-163">Project</span><span class="sxs-lookup"><span data-stu-id="2d234-163">Project</span></span></p></th>
<th><p><span data-ttu-id="2d234-164">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="2d234-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2d234-165">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="2d234-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="2d234-166">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="2d234-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2d234-167">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="2d234-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-168">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="2d234-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2d234-169">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2d234-170">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="2d234-170">Month</span></span></p></td>
<td><p><span data-ttu-id="2d234-171">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-172">500</span><span class="sxs-lookup"><span data-stu-id="2d234-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-173">Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="2d234-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="2d234-174">Sitten luot seuraavat ylläpitosopimukset.</span><span class="sxs-lookup"><span data-stu-id="2d234-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="2d234-175">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="2d234-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2d234-176">Project</span><span class="sxs-lookup"><span data-stu-id="2d234-176">Project</span></span></p></th>
<th><p><span data-ttu-id="2d234-177">Ylläpitosopimusryhmä</span><span class="sxs-lookup"><span data-stu-id="2d234-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="2d234-178">Luokka</span><span class="sxs-lookup"><span data-stu-id="2d234-178">Category</span></span></p></th>
<th><p><span data-ttu-id="2d234-179">Valuutta</span><span class="sxs-lookup"><span data-stu-id="2d234-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="2d234-180">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="2d234-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="2d234-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-182">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-182">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="2d234-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2d234-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2d234-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2d234-185">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-186">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="2d234-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="2d234-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-188">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-188">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="2d234-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2d234-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2d234-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2d234-191">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-192">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="2d234-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-193">Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:</span><span class="sxs-lookup"><span data-stu-id="2d234-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="2d234-194">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="2d234-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="2d234-195">Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="2d234-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="2d234-196">Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="2d234-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="2d234-197">Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="2d234-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="2d234-198">Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="2d234-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="2d234-199">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="2d234-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="2d234-200">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="2d234-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2d234-201">Project</span><span class="sxs-lookup"><span data-stu-id="2d234-201">Project</span></span></p></th>
<th><p><span data-ttu-id="2d234-202">Luokka</span><span class="sxs-lookup"><span data-stu-id="2d234-202">Category</span></span></p></th>
<th><p><span data-ttu-id="2d234-203">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="2d234-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="2d234-204">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="2d234-204">End date</span></span></p></th>
<th><p><span data-ttu-id="2d234-205">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="2d234-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2d234-206">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="2d234-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-207">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="2d234-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2d234-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="2d234-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-209">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-209">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2d234-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2d234-211">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-212">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-213">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-214">500</span><span class="sxs-lookup"><span data-stu-id="2d234-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-215">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="2d234-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2d234-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="2d234-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-217">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-217">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2d234-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2d234-219">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-220">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-221">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-222">500</span><span class="sxs-lookup"><span data-stu-id="2d234-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-223">Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030.</span><span class="sxs-lookup"><span data-stu-id="2d234-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="2d234-224">Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="2d234-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="2d234-225">Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="2d234-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="2d234-226">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="2d234-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2d234-227">Luokka</span><span class="sxs-lookup"><span data-stu-id="2d234-227">Category</span></span></p></th>
<th><p><span data-ttu-id="2d234-228">Project</span><span class="sxs-lookup"><span data-stu-id="2d234-228">Project</span></span></p></th>
<th><p><span data-ttu-id="2d234-229">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="2d234-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2d234-230">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="2d234-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="2d234-231">Valuutta</span><span class="sxs-lookup"><span data-stu-id="2d234-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="2d234-232">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="2d234-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-233">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2d234-234">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2d234-235">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="2d234-235">Month</span></span></p></td>
<td><p><span data-ttu-id="2d234-236">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-237">500</span><span class="sxs-lookup"><span data-stu-id="2d234-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-238">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2d234-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2d234-240">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2d234-241">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="2d234-241">Month</span></span></p></td>
<td><p><span data-ttu-id="2d234-242">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-243">550</span><span class="sxs-lookup"><span data-stu-id="2d234-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-244">Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="2d234-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="2d234-245">Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.</span><span class="sxs-lookup"><span data-stu-id="2d234-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="2d234-246">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="2d234-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="2d234-247">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="2d234-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2d234-248">Project</span><span class="sxs-lookup"><span data-stu-id="2d234-248">Project</span></span></p></th>
<th><p><span data-ttu-id="2d234-249">Luokka</span><span class="sxs-lookup"><span data-stu-id="2d234-249">Category</span></span></p></th>
<th><p><span data-ttu-id="2d234-250">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="2d234-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="2d234-251">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="2d234-251">End date</span></span></p></th>
<th><p><span data-ttu-id="2d234-252">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="2d234-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2d234-253">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="2d234-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d234-254">28.7.2007</span><span class="sxs-lookup"><span data-stu-id="2d234-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="2d234-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="2d234-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-256">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-256">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2d234-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2d234-258">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="2d234-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2d234-259">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="2d234-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2d234-260">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-261">550</span><span class="sxs-lookup"><span data-stu-id="2d234-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d234-262">28.7.2008</span><span class="sxs-lookup"><span data-stu-id="2d234-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="2d234-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="2d234-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2d234-264">9030</span><span class="sxs-lookup"><span data-stu-id="2d234-264">9030</span></span></p></td>
<td><p><span data-ttu-id="2d234-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2d234-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2d234-266">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="2d234-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2d234-267">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="2d234-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2d234-268">Euro</span><span class="sxs-lookup"><span data-stu-id="2d234-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="2d234-269">500</span><span class="sxs-lookup"><span data-stu-id="2d234-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d234-270">Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta.</span><span class="sxs-lookup"><span data-stu-id="2d234-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="2d234-271">Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.</span><span class="sxs-lookup"><span data-stu-id="2d234-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d234-272">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2d234-272">See also</span></span>

[<span data-ttu-id="2d234-273">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="2d234-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


