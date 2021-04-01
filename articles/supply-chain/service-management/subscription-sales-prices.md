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
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242298"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="edff9-103">Ylläpitosopimuksen myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="edff9-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="edff9-104">Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.</span><span class="sxs-lookup"><span data-stu-id="edff9-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="edff9-105">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="edff9-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="edff9-106">Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.</span><span class="sxs-lookup"><span data-stu-id="edff9-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="edff9-107">Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella.</span><span class="sxs-lookup"><span data-stu-id="edff9-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="edff9-108">Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="edff9-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="edff9-109">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="edff9-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="edff9-110"><strong>Luokka</strong></span><span class="sxs-lookup"><span data-stu-id="edff9-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="edff9-111"><strong>Projektin tunnus</strong></span><span class="sxs-lookup"><span data-stu-id="edff9-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="edff9-112"><strong>Ylläpitosopimus</strong></span><span class="sxs-lookup"><span data-stu-id="edff9-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="edff9-113"><strong>Myyntivaluutta</strong></span><span class="sxs-lookup"><span data-stu-id="edff9-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="edff9-114"><strong>Kausikoodi</strong></span><span class="sxs-lookup"><span data-stu-id="edff9-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-115">1</span><span class="sxs-lookup"><span data-stu-id="edff9-115">1</span></span></p></td>
<td><p><span data-ttu-id="edff9-116">X</span><span class="sxs-lookup"><span data-stu-id="edff9-116">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-117">X</span><span class="sxs-lookup"><span data-stu-id="edff9-117">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-118">X</span><span class="sxs-lookup"><span data-stu-id="edff9-118">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-119">X</span><span class="sxs-lookup"><span data-stu-id="edff9-119">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-120">X</span><span class="sxs-lookup"><span data-stu-id="edff9-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-121">2</span><span class="sxs-lookup"><span data-stu-id="edff9-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-122">X</span><span class="sxs-lookup"><span data-stu-id="edff9-122">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-123">X</span><span class="sxs-lookup"><span data-stu-id="edff9-123">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-124">X</span><span class="sxs-lookup"><span data-stu-id="edff9-124">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-125">X</span><span class="sxs-lookup"><span data-stu-id="edff9-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edff9-126">3</span><span class="sxs-lookup"><span data-stu-id="edff9-126">3</span></span></p></td>
<td><p><span data-ttu-id="edff9-127">X</span><span class="sxs-lookup"><span data-stu-id="edff9-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-128">X</span><span class="sxs-lookup"><span data-stu-id="edff9-128">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-129">X</span><span class="sxs-lookup"><span data-stu-id="edff9-129">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-130">X</span><span class="sxs-lookup"><span data-stu-id="edff9-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-131">4</span><span class="sxs-lookup"><span data-stu-id="edff9-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-132">X</span><span class="sxs-lookup"><span data-stu-id="edff9-132">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-133">X</span><span class="sxs-lookup"><span data-stu-id="edff9-133">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-134">X</span><span class="sxs-lookup"><span data-stu-id="edff9-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edff9-135">5</span><span class="sxs-lookup"><span data-stu-id="edff9-135">5</span></span></p></td>
<td><p><span data-ttu-id="edff9-136">X</span><span class="sxs-lookup"><span data-stu-id="edff9-136">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-137">X</span><span class="sxs-lookup"><span data-stu-id="edff9-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-138">X</span><span class="sxs-lookup"><span data-stu-id="edff9-138">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-139">X</span><span class="sxs-lookup"><span data-stu-id="edff9-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-140">6</span><span class="sxs-lookup"><span data-stu-id="edff9-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-141">X</span><span class="sxs-lookup"><span data-stu-id="edff9-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-142">X</span><span class="sxs-lookup"><span data-stu-id="edff9-142">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-143">X</span><span class="sxs-lookup"><span data-stu-id="edff9-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edff9-144">7</span><span class="sxs-lookup"><span data-stu-id="edff9-144">7</span></span></p></td>
<td><p><span data-ttu-id="edff9-145">X</span><span class="sxs-lookup"><span data-stu-id="edff9-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-146">X</span><span class="sxs-lookup"><span data-stu-id="edff9-146">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-147">X</span><span class="sxs-lookup"><span data-stu-id="edff9-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-148">8</span><span class="sxs-lookup"><span data-stu-id="edff9-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="edff9-149">X</span><span class="sxs-lookup"><span data-stu-id="edff9-149">X</span></span></p></td>
<td><p><span data-ttu-id="edff9-150">X</span><span class="sxs-lookup"><span data-stu-id="edff9-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-151">Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.</span><span class="sxs-lookup"><span data-stu-id="edff9-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="edff9-152">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="edff9-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="edff9-153">Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin.</span><span class="sxs-lookup"><span data-stu-id="edff9-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="edff9-154">Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.</span><span class="sxs-lookup"><span data-stu-id="edff9-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="edff9-155">Ylläpitosopimusmaksun myyntihinnat</span><span class="sxs-lookup"><span data-stu-id="edff9-155">Subscription fee sales prices</span></span>

<span data-ttu-id="edff9-156">Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="edff9-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="edff9-157">Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.</span><span class="sxs-lookup"><span data-stu-id="edff9-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="edff9-158">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="edff9-158">Example</span></span>

<span data-ttu-id="edff9-159">Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="edff9-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="edff9-160">**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="edff9-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="edff9-161">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="edff9-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="edff9-162">Luokka</span><span class="sxs-lookup"><span data-stu-id="edff9-162">Category</span></span></p></th>
<th><p><span data-ttu-id="edff9-163">Project</span><span class="sxs-lookup"><span data-stu-id="edff9-163">Project</span></span></p></th>
<th><p><span data-ttu-id="edff9-164">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="edff9-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="edff9-165">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="edff9-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="edff9-166">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="edff9-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="edff9-167">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="edff9-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-168">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="edff9-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="edff9-169">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="edff9-170">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="edff9-170">Month</span></span></p></td>
<td><p><span data-ttu-id="edff9-171">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-172">500</span><span class="sxs-lookup"><span data-stu-id="edff9-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-173">Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="edff9-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="edff9-174">Sitten luot seuraavat ylläpitosopimukset.</span><span class="sxs-lookup"><span data-stu-id="edff9-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="edff9-175">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="edff9-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="edff9-176">Project</span><span class="sxs-lookup"><span data-stu-id="edff9-176">Project</span></span></p></th>
<th><p><span data-ttu-id="edff9-177">Ylläpitosopimusryhmä</span><span class="sxs-lookup"><span data-stu-id="edff9-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="edff9-178">Luokka</span><span class="sxs-lookup"><span data-stu-id="edff9-178">Category</span></span></p></th>
<th><p><span data-ttu-id="edff9-179">Valuutta</span><span class="sxs-lookup"><span data-stu-id="edff9-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="edff9-180">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="edff9-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="edff9-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-182">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-182">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="edff9-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="edff9-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="edff9-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="edff9-185">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-186">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="edff9-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="edff9-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-188">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-188">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="edff9-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="edff9-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="edff9-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="edff9-191">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-192">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="edff9-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-193">Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:</span><span class="sxs-lookup"><span data-stu-id="edff9-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="edff9-194">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="edff9-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="edff9-195">Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.</span><span class="sxs-lookup"><span data-stu-id="edff9-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="edff9-196">Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="edff9-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="edff9-197">Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="edff9-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="edff9-198">Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="edff9-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="edff9-199">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="edff9-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="edff9-200">Huollon ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="edff9-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="edff9-201">Project</span><span class="sxs-lookup"><span data-stu-id="edff9-201">Project</span></span></p></th>
<th><p><span data-ttu-id="edff9-202">Luokka</span><span class="sxs-lookup"><span data-stu-id="edff9-202">Category</span></span></p></th>
<th><p><span data-ttu-id="edff9-203">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="edff9-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="edff9-204">Päättymispäivä</span><span class="sxs-lookup"><span data-stu-id="edff9-204">End date</span></span></p></th>
<th><p><span data-ttu-id="edff9-205">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="edff9-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="edff9-206">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="edff9-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-207">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="edff9-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="edff9-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="edff9-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-209">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-209">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="edff9-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="edff9-211">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-212">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-213">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-214">500</span><span class="sxs-lookup"><span data-stu-id="edff9-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-215">28.8.2006</span><span class="sxs-lookup"><span data-stu-id="edff9-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="edff9-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="edff9-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-217">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-217">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="edff9-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="edff9-219">1.1.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-220">31.3.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-221">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-222">500</span><span class="sxs-lookup"><span data-stu-id="edff9-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-223">Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030.</span><span class="sxs-lookup"><span data-stu-id="edff9-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="edff9-224">Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="edff9-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="edff9-225">Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="edff9-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="edff9-226">Voimassaolo alkaa</span><span class="sxs-lookup"><span data-stu-id="edff9-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="edff9-227">Luokka</span><span class="sxs-lookup"><span data-stu-id="edff9-227">Category</span></span></p></th>
<th><p><span data-ttu-id="edff9-228">Project</span><span class="sxs-lookup"><span data-stu-id="edff9-228">Project</span></span></p></th>
<th><p><span data-ttu-id="edff9-229">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="edff9-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="edff9-230">Kausikoodi</span><span class="sxs-lookup"><span data-stu-id="edff9-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="edff9-231">Valuutta</span><span class="sxs-lookup"><span data-stu-id="edff9-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="edff9-232">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="edff9-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-233">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="edff9-234">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="edff9-235">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="edff9-235">Month</span></span></p></td>
<td><p><span data-ttu-id="edff9-236">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-237">500</span><span class="sxs-lookup"><span data-stu-id="edff9-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-238">28.8.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="edff9-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="edff9-240">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="edff9-241">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="edff9-241">Month</span></span></p></td>
<td><p><span data-ttu-id="edff9-242">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-243">550</span><span class="sxs-lookup"><span data-stu-id="edff9-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-244">Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille.</span><span class="sxs-lookup"><span data-stu-id="edff9-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="edff9-245">Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.</span><span class="sxs-lookup"><span data-stu-id="edff9-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="edff9-246">Projektipäiväys</span><span class="sxs-lookup"><span data-stu-id="edff9-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="edff9-247">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="edff9-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="edff9-248">Project</span><span class="sxs-lookup"><span data-stu-id="edff9-248">Project</span></span></p></th>
<th><p><span data-ttu-id="edff9-249">Luokka</span><span class="sxs-lookup"><span data-stu-id="edff9-249">Category</span></span></p></th>
<th><p><span data-ttu-id="edff9-250">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="edff9-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="edff9-251">Päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="edff9-251">End date</span></span></p></th>
<th><p><span data-ttu-id="edff9-252">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="edff9-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="edff9-253">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="edff9-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edff9-254">28.7.2007</span><span class="sxs-lookup"><span data-stu-id="edff9-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="edff9-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="edff9-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-256">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-256">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="edff9-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="edff9-258">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="edff9-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="edff9-259">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="edff9-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="edff9-260">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-261">550</span><span class="sxs-lookup"><span data-stu-id="edff9-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edff9-262">28.7.2008</span><span class="sxs-lookup"><span data-stu-id="edff9-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="edff9-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="edff9-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="edff9-264">9030</span><span class="sxs-lookup"><span data-stu-id="edff9-264">9030</span></span></p></td>
<td><p><span data-ttu-id="edff9-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="edff9-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="edff9-266">1.1.2008</span><span class="sxs-lookup"><span data-stu-id="edff9-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="edff9-267">31.3.2008</span><span class="sxs-lookup"><span data-stu-id="edff9-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="edff9-268">Euro</span><span class="sxs-lookup"><span data-stu-id="edff9-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="edff9-269">500</span><span class="sxs-lookup"><span data-stu-id="edff9-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="edff9-270">Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta.</span><span class="sxs-lookup"><span data-stu-id="edff9-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="edff9-271">Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.</span><span class="sxs-lookup"><span data-stu-id="edff9-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="edff9-272">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="edff9-272">See also</span></span>

[<span data-ttu-id="edff9-273">Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen</span><span class="sxs-lookup"><span data-stu-id="edff9-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]