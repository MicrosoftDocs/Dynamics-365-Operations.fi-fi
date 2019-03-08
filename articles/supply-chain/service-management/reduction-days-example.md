---
title: Esimerkki vähennyspäivistä
description: Esimerkki vähennyspäivistä.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "334102"
---
# <a name="reduction-days-example"></a><span data-ttu-id="dc265-103">Esimerkki vähennyspäivistä</span><span class="sxs-lookup"><span data-stu-id="dc265-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dc265-104">Olet luonut asiakkaan ylläpitosopimukselle ylläpitosopimustapahtuman seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="dc265-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="dc265-105">Päivämäärästä</span><span class="sxs-lookup"><span data-stu-id="dc265-105">From date</span></span></p></th>
<th><p><span data-ttu-id="dc265-106">Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="dc265-106">To date</span></span></p></th>
<th><p><span data-ttu-id="dc265-107">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="dc265-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="dc265-108">Ylläpitosopimustyyppi</span><span class="sxs-lookup"><span data-stu-id="dc265-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="dc265-109">Project</span><span class="sxs-lookup"><span data-stu-id="dc265-109">Project</span></span></p></th>
<th><p><span data-ttu-id="dc265-110">Luokka</span><span class="sxs-lookup"><span data-stu-id="dc265-110">Category</span></span></p></th>
<th><p><span data-ttu-id="dc265-111">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="dc265-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="dc265-112">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="dc265-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc265-113">01. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="dc265-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="dc265-114">31. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="dc265-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="dc265-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="dc265-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="dc265-116"><strong>Säännöllinen</strong></span><span class="sxs-lookup"><span data-stu-id="dc265-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="dc265-117">9013</span><span class="sxs-lookup"><span data-stu-id="dc265-117">9013</span></span></p></td>
<td><p><span data-ttu-id="dc265-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="dc265-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="dc265-119">Euro</span><span class="sxs-lookup"><span data-stu-id="dc265-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="dc265-120">200,00</span><span class="sxs-lookup"><span data-stu-id="dc265-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc265-121">Asiakas raportoi, että hän ei tarvitse huollon kattavuutta kahden päivän aikana (maaliskuun 10. ja 11. päivänä).</span><span class="sxs-lookup"><span data-stu-id="dc265-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="dc265-122">Suostut pienentämään ylläpitosopimusta näiden kahden päivän aikana.</span><span class="sxs-lookup"><span data-stu-id="dc265-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="dc265-123">Luot uuden **Vähennyspäivät**-tyyppisen tapahtuman seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="dc265-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="dc265-124">Päivämäärästä</span><span class="sxs-lookup"><span data-stu-id="dc265-124">From date</span></span></p></th>
<th><p><span data-ttu-id="dc265-125">Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="dc265-125">To date</span></span></p></th>
<th><p><span data-ttu-id="dc265-126">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="dc265-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="dc265-127">Ylläpitosopimustyyppi</span><span class="sxs-lookup"><span data-stu-id="dc265-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="dc265-128">Project</span><span class="sxs-lookup"><span data-stu-id="dc265-128">Project</span></span></p></th>
<th><p><span data-ttu-id="dc265-129">Luokka</span><span class="sxs-lookup"><span data-stu-id="dc265-129">Category</span></span></p></th>
<th><p><span data-ttu-id="dc265-130">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="dc265-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="dc265-131">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="dc265-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc265-132">10. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="dc265-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="dc265-133">11. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="dc265-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="dc265-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="dc265-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="dc265-135"><strong>Vähennyspäivät</strong></span><span class="sxs-lookup"><span data-stu-id="dc265-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="dc265-136">9013</span><span class="sxs-lookup"><span data-stu-id="dc265-136">9013</span></span></p></td>
<td><p><span data-ttu-id="dc265-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="dc265-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="dc265-138">Euro</span><span class="sxs-lookup"><span data-stu-id="dc265-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="dc265-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="dc265-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc265-140">Kun maaliskuun 2011 tapahtumat laskutetaan, 200 euron myyntihinnasta vähennetään 12,90 euroa.</span><span class="sxs-lookup"><span data-stu-id="dc265-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="dc265-141">Ylläpitosopimustapahtuman veloitettava summa on siis 187,10 euroa, ja kaksi tapahtumaa laskutetaan yhteissummalla 187,10 euroa.</span><span class="sxs-lookup"><span data-stu-id="dc265-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc265-142">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="dc265-142">See also</span></span>

[<span data-ttu-id="dc265-143">Ylläpitosopimusmaksujen päivien vähentäminen</span><span class="sxs-lookup"><span data-stu-id="dc265-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


