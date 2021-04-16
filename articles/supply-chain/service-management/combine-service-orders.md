---
title: Yhdistä huoltotilaukset
description: Voit yhdistää huoltotilauksia.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41b4a3234e4104372f1052d89c2417984e9cd10d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840554"
---
# <a name="combine-service-orders"></a><span data-ttu-id="4f126-103">Yhdistä huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="4f126-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4f126-104">Kun luot huoltotilausrivejä automaattisesti **Huoltosopimukset**-lomakkeessa, voit valita jonkin seuraavista vaihtoehdoista määrittääksesi, miten haluat ryhmitellä ne:</span><span class="sxs-lookup"><span data-stu-id="4f126-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="4f126-105">**Huoltosopimuksen mukaan**</span><span class="sxs-lookup"><span data-stu-id="4f126-105">**By service agreement**</span></span>

  - <span data-ttu-id="4f126-106">**Huoltotehtävän mukaan**</span><span class="sxs-lookup"><span data-stu-id="4f126-106">**By service task**</span></span>

  - <span data-ttu-id="4f126-107">**Työntekijän mukaan**</span><span class="sxs-lookup"><span data-stu-id="4f126-107">**By employee**</span></span>

  - <span data-ttu-id="4f126-108">**Huoltokohteen mukaan**</span><span class="sxs-lookup"><span data-stu-id="4f126-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="4f126-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4f126-109">Example</span></span>

<span data-ttu-id="4f126-110">Luot huoltosopimuksen alkamispäivämäärällä 31.3.2007.</span><span class="sxs-lookup"><span data-stu-id="4f126-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="4f126-111">Valitset **Yhdistä huoltotilaukset** -kentässä **Huoltokohteen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="4f126-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="4f126-112">Sitten luot seuraavat huoltosopimusrivit:</span><span class="sxs-lookup"><span data-stu-id="4f126-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="4f126-113">Sopimusrivin numero</span><span class="sxs-lookup"><span data-stu-id="4f126-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="4f126-114">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="4f126-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="4f126-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4f126-115">Description</span></span></p></th>
<th><p><span data-ttu-id="4f126-116">Väli</span><span class="sxs-lookup"><span data-stu-id="4f126-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="4f126-117">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="4f126-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="4f126-118">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="4f126-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f126-119">1</span><span class="sxs-lookup"><span data-stu-id="4f126-119">1</span></span></p></td>
<td><p><span data-ttu-id="4f126-120"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="4f126-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="4f126-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="4f126-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="4f126-122">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="4f126-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="4f126-123">X-1</span><span class="sxs-lookup"><span data-stu-id="4f126-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="4f126-124">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="4f126-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f126-125">2</span><span class="sxs-lookup"><span data-stu-id="4f126-125">2</span></span></p></td>
<td><p><span data-ttu-id="4f126-126"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="4f126-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="4f126-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="4f126-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="4f126-128">Kaksi kertaa viikossa</span><span class="sxs-lookup"><span data-stu-id="4f126-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="4f126-129">X-2</span><span class="sxs-lookup"><span data-stu-id="4f126-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="4f126-130">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="4f126-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f126-131">3</span><span class="sxs-lookup"><span data-stu-id="4f126-131">3</span></span></p></td>
<td><p><span data-ttu-id="4f126-132"><strong>Tunti</strong></span><span class="sxs-lookup"><span data-stu-id="4f126-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="4f126-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="4f126-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="4f126-134">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="4f126-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="4f126-135">X-2</span><span class="sxs-lookup"><span data-stu-id="4f126-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="4f126-136">1.4.2007</span><span class="sxs-lookup"><span data-stu-id="4f126-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f126-137">Et määritä yhdellekään huoltosopimusriville aikaikkunaa.</span><span class="sxs-lookup"><span data-stu-id="4f126-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="4f126-138">Sen vuoksi huoltotilausrivejä ei siirretä niiden laskentapäivästä.</span><span class="sxs-lookup"><span data-stu-id="4f126-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="4f126-139">Tämän jälkeen luot **Luo huoltotilauksia** -lomakkeessa huoltotilausrivit 1.4. - 30.4.2007 väliselle ajalle.</span><span class="sxs-lookup"><span data-stu-id="4f126-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="4f126-140">Luotavien huoltotilausten määrä on 10.</span><span class="sxs-lookup"><span data-stu-id="4f126-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="4f126-141">Koska valitsemasi yhdistetty asetus oli **Huoltokohteen mukaan**, kaikilla luoduilla huoltotilauksilla on vain sellaisia huoltotilausrivejä, joilla on yksi tietty huoltokohde.</span><span class="sxs-lookup"><span data-stu-id="4f126-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="4f126-142">Huoltosopimuksesta luotavat huoltotilausrivit, joilla on sama huoltopäivämäärä ja sama kohde, yhdistetään samaan huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="4f126-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4f126-143">Tässä esimerkissä <STRONG>Huoltoparametrit</STRONG>-lomakkeessa määritetyllä kalenterilla ei ole suljettuja päiviä.</span><span class="sxs-lookup"><span data-stu-id="4f126-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="4f126-144">Huoltotilausrivien lisäryhmittely huoltotilauksiin tapahtuu huoltosopimusriveillä määrittämiesi aikaikkunoiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="4f126-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f126-145">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4f126-145">See also</span></span>

[<span data-ttu-id="4f126-146">Automaattisesti luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="4f126-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]