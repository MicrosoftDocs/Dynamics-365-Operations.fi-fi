---
title: Yhdistä huoltotilaukset
description: Voit yhdistää huoltotilauksia.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17fbed59b1fe7bec80f25f74451872efd61bed62
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426861"
---
# <a name="combine-service-orders"></a><span data-ttu-id="6f61a-103">Yhdistä huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="6f61a-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6f61a-104">Kun luot huoltotilausrivejä automaattisesti **Huoltosopimukset**-lomakkeessa, voit valita jonkin seuraavista vaihtoehdoista määrittääksesi, miten haluat ryhmitellä ne:</span><span class="sxs-lookup"><span data-stu-id="6f61a-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="6f61a-105">**Huoltosopimuksen mukaan**</span><span class="sxs-lookup"><span data-stu-id="6f61a-105">**By service agreement**</span></span>

  - <span data-ttu-id="6f61a-106">**Huoltotehtävän mukaan**</span><span class="sxs-lookup"><span data-stu-id="6f61a-106">**By service task**</span></span>

  - <span data-ttu-id="6f61a-107">**Työntekijän mukaan**</span><span class="sxs-lookup"><span data-stu-id="6f61a-107">**By employee**</span></span>

  - <span data-ttu-id="6f61a-108">**Huoltokohteen mukaan**</span><span class="sxs-lookup"><span data-stu-id="6f61a-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="6f61a-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="6f61a-109">Example</span></span>

<span data-ttu-id="6f61a-110">Luot huoltosopimuksen alkamispäivämäärällä 31.3.2007.</span><span class="sxs-lookup"><span data-stu-id="6f61a-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="6f61a-111">Valitset **Yhdistä huoltotilaukset** -kentässä **Huoltokohteen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="6f61a-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="6f61a-112">Sitten luot seuraavat huoltosopimusrivit:</span><span class="sxs-lookup"><span data-stu-id="6f61a-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="6f61a-113">Sopimusrivin numero</span><span class="sxs-lookup"><span data-stu-id="6f61a-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="6f61a-114">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="6f61a-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="6f61a-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6f61a-115">Description</span></span></p></th>
<th><p><span data-ttu-id="6f61a-116">Väli</span><span class="sxs-lookup"><span data-stu-id="6f61a-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="6f61a-117">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="6f61a-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="6f61a-118">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="6f61a-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f61a-119">1</span><span class="sxs-lookup"><span data-stu-id="6f61a-119">1</span></span></p></td>
<td><p><span data-ttu-id="6f61a-120"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="6f61a-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="6f61a-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="6f61a-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="6f61a-122">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="6f61a-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="6f61a-123">X-1</span><span class="sxs-lookup"><span data-stu-id="6f61a-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="6f61a-124">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="6f61a-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f61a-125">2</span><span class="sxs-lookup"><span data-stu-id="6f61a-125">2</span></span></p></td>
<td><p><span data-ttu-id="6f61a-126"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="6f61a-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="6f61a-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="6f61a-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="6f61a-128">Kaksi kertaa viikossa</span><span class="sxs-lookup"><span data-stu-id="6f61a-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="6f61a-129">X-2</span><span class="sxs-lookup"><span data-stu-id="6f61a-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="6f61a-130">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="6f61a-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f61a-131">3</span><span class="sxs-lookup"><span data-stu-id="6f61a-131">3</span></span></p></td>
<td><p><span data-ttu-id="6f61a-132"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="6f61a-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="6f61a-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="6f61a-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="6f61a-134">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="6f61a-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="6f61a-135">X-2</span><span class="sxs-lookup"><span data-stu-id="6f61a-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="6f61a-136">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="6f61a-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6f61a-137">Et määritä yhdellekään huoltosopimusriville aikaikkunaa.</span><span class="sxs-lookup"><span data-stu-id="6f61a-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="6f61a-138">Sen vuoksi huoltotilausrivejä ei siirretä niiden laskentapäivästä.</span><span class="sxs-lookup"><span data-stu-id="6f61a-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="6f61a-139">Tämän jälkeen luot **Luo huoltotilauksia** -lomakkeessa huoltotilausrivit 1.4. - 30.4.2007 väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="6f61a-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="6f61a-140">Luotavien huoltotilausten määrä on 10.</span><span class="sxs-lookup"><span data-stu-id="6f61a-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="6f61a-141">Koska valitsemasi yhdistetty asetus oli **Huoltokohteen mukaan**, kaikilla luoduilla huoltotilauksilla on vain sellaisia huoltotilausrivejä, joilla on yksi tietty huoltokohde.</span><span class="sxs-lookup"><span data-stu-id="6f61a-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="6f61a-142">Huoltosopimuksesta luotavat huoltotilausrivit, joilla on sama huoltopäivämäärä ja sama kohde, yhdistetään samaan huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6f61a-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6f61a-143">Tässä esimerkissä <STRONG>Huoltoparametrit</STRONG>-lomakkeessa määritetyllä kalenterilla ei ole suljettuja päiviä.</span><span class="sxs-lookup"><span data-stu-id="6f61a-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="6f61a-144">Huoltotilausrivien lisäryhmittely huoltotilauksiin tapahtuu huoltosopimusriveillä määrittämiesi aikaikkunoiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6f61a-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f61a-145">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6f61a-145">See also</span></span>

[<span data-ttu-id="6f61a-146">Automaattisesti luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="6f61a-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


