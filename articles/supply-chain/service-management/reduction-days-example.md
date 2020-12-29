---
title: Esimerkki vähennyspäivistä
description: Esimerkki vähennyspäivistä.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426817"
---
# <a name="reduction-days-example"></a><span data-ttu-id="b909e-103">Esimerkki vähennyspäivistä</span><span class="sxs-lookup"><span data-stu-id="b909e-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b909e-104">Olet luonut asiakkaan ylläpitosopimukselle ylläpitosopimustapahtuman seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b909e-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="b909e-105">Päivämäärästä</span><span class="sxs-lookup"><span data-stu-id="b909e-105">From date</span></span></p></th>
<th><p><span data-ttu-id="b909e-106">Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="b909e-106">To date</span></span></p></th>
<th><p><span data-ttu-id="b909e-107">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b909e-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b909e-108">Ylläpitosopimustyyppi</span><span class="sxs-lookup"><span data-stu-id="b909e-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="b909e-109">Project</span><span class="sxs-lookup"><span data-stu-id="b909e-109">Project</span></span></p></th>
<th><p><span data-ttu-id="b909e-110">Luokka</span><span class="sxs-lookup"><span data-stu-id="b909e-110">Category</span></span></p></th>
<th><p><span data-ttu-id="b909e-111">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="b909e-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b909e-112">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b909e-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b909e-113">01. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="b909e-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="b909e-114">31. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="b909e-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="b909e-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="b909e-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="b909e-116"><strong>Säännöllinen</strong></span><span class="sxs-lookup"><span data-stu-id="b909e-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="b909e-117">9013</span><span class="sxs-lookup"><span data-stu-id="b909e-117">9013</span></span></p></td>
<td><p><span data-ttu-id="b909e-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b909e-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b909e-119">Euro</span><span class="sxs-lookup"><span data-stu-id="b909e-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="b909e-120">200,00</span><span class="sxs-lookup"><span data-stu-id="b909e-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b909e-121">Asiakas raportoi, että hän ei tarvitse huollon kattavuutta kahden päivän aikana (maaliskuun 10. ja 11. päivänä).</span><span class="sxs-lookup"><span data-stu-id="b909e-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="b909e-122">Suostut pienentämään ylläpitosopimusta näiden kahden päivän aikana.</span><span class="sxs-lookup"><span data-stu-id="b909e-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="b909e-123">Luot uuden **Vähennyspäivät**-tyyppisen tapahtuman seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b909e-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="b909e-124">Päivämäärästä</span><span class="sxs-lookup"><span data-stu-id="b909e-124">From date</span></span></p></th>
<th><p><span data-ttu-id="b909e-125">Päivämäärään</span><span class="sxs-lookup"><span data-stu-id="b909e-125">To date</span></span></p></th>
<th><p><span data-ttu-id="b909e-126">Ylläpitosopimus</span><span class="sxs-lookup"><span data-stu-id="b909e-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="b909e-127">Ylläpitosopimustyyppi</span><span class="sxs-lookup"><span data-stu-id="b909e-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="b909e-128">Project</span><span class="sxs-lookup"><span data-stu-id="b909e-128">Project</span></span></p></th>
<th><p><span data-ttu-id="b909e-129">Luokka</span><span class="sxs-lookup"><span data-stu-id="b909e-129">Category</span></span></p></th>
<th><p><span data-ttu-id="b909e-130">Myyntivaluutta</span><span class="sxs-lookup"><span data-stu-id="b909e-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="b909e-131">Myyntihinta</span><span class="sxs-lookup"><span data-stu-id="b909e-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b909e-132">10. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="b909e-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="b909e-133">11. maaliskuuta 2011</span><span class="sxs-lookup"><span data-stu-id="b909e-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="b909e-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="b909e-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="b909e-135"><strong>Vähennyspäivät</strong></span><span class="sxs-lookup"><span data-stu-id="b909e-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="b909e-136">9013</span><span class="sxs-lookup"><span data-stu-id="b909e-136">9013</span></span></p></td>
<td><p><span data-ttu-id="b909e-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="b909e-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="b909e-138">Euro</span><span class="sxs-lookup"><span data-stu-id="b909e-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="b909e-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="b909e-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b909e-140">Kun maaliskuun 2011 tapahtumat laskutetaan, 200 euron myyntihinnasta vähennetään 12,90 euroa.</span><span class="sxs-lookup"><span data-stu-id="b909e-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="b909e-141">Ylläpitosopimustapahtuman veloitettava summa on siis 187,10 euroa, ja kaksi tapahtumaa laskutetaan yhteissummalla 187,10 euroa.</span><span class="sxs-lookup"><span data-stu-id="b909e-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="b909e-142">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="b909e-142">See also</span></span>

[<span data-ttu-id="b909e-143">Ylläpitosopimusmaksujen päivien vähentäminen</span><span class="sxs-lookup"><span data-stu-id="b909e-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


